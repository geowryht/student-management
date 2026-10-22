
<script>
export default {
    props: ['studentEdit'],

    emits: ['update-student', 'close'],

    data() {
        return {
            form: {
                name: '',
                age: '',
                address: '',
                contact: '',
                status: 'Active'
            },

        }
    },

    methods: {
        loadStudent() {
            if (this.student) {
                this.form = { ...this.student }
            }
        },

        updateStudent() {
            this.$emit('update-student', { ...this.form })
        },

        closeModal(i) {
            this.$emit('close', i)
        }
    },

    mounted() {
        this.loadStudent()
    }
}
</script>

<template>
    <div  class="fixed inset-0 z-50 flex items-center justify-center bg-black/50 p-4">

        <div class="w-full max-w-lg rounded-xl bg-white p-6 shadow-2xl">

            <!-- Header -->
            <div class="mb-6 flex items-center justify-between">
                <h2 class="text-2xl font-bold text-gray-800">
                    Edit Student
                </h2>

                <button
                    type="button"
                    @click="closeModal"
                    class="text-2xl text-gray-500 hover:text-red-500 cursor-pointer"
                >
                    X
                </button>
            </div>

            <!-- Form -->
            <form @submit.prevent="updateStudent" class="space-y-4">

                <!-- Name -->
                <div>
                    <label class="mb-1 block font-semibold text-gray-700">
                        Name
                    </label>

                    <input
                        v-model="form.name"
                        type="text"
                        required
                        placeholder="Enter student name"
                        class="w-full rounded-lg border border-gray-300 px-4 py-2 outline-none focus:border-blue-500"
                    />
                </div>
                <!-- Age -->
                <div>
                    <label class="mb-1 block font-semibold text-gray-700">
                        Age
                    </label>

                    <input
                        v-model.number="form.age"
                        type="number"
                        min="1"
                        required
                        placeholder="Enter age"
                        class="w-full rounded-lg border border-gray-300 px-4 py-2 outline-none focus:border-blue-500"
                    />
                </div>
                <!-- Address -->
                <div>
                    <label class="mb-1 block font-semibold text-gray-700">
                        Address
                    </label>

                    <input
                        v-model="form.address"
                        type="text"
                        required
                        placeholder="Enter address"
                        class="w-full rounded-lg border border-gray-300 px-4 py-2 outline-none focus:border-blue-500"
                    />
                </div>
                <!-- contact -->
                <div>
                    <label class="mb-1 block font-semibold text-gray-700">
                        Contact
                    </label>

                    <input
                        v-model="form.contact"
                        type="tel"
                        required
                        placeholder="Enter contact number"
                        class="w-full rounded-lg border border-gray-300 px-4 py-2 outline-none focus:border-blue-500"
                    />
                </div>
                <!-- Status -->
                <div>
                    <label class="mb-1 block font-semibold text-gray-700">
                        Status
                    </label>

                    <select
                        v-model="form.status"
                        required
                        class="w-full rounded-lg border border-gray-300 bg-white px-4 py-2 outline-none focus:border-blue-500"
                    >
                        <option value="Active">Active</option>
                        <option value="Inactive">Inactive</option>
                    </select>
                </div>

                <!-- Buttons -->
                <div class="flex justify-end gap-3 pt-4">
                    <button
                        type="button"
                        @click="closeModal(false)"
                        class="rounded-lg border border-gray-300 px-5 py-2 font-semibold text-gray-700 hover:bg-gray-100 cursor-pointer"
                    >
                        Cancel
                    </button>

                    <button
                        type="submit"
                        class="rounded-lg bg-blue-700 px-5 py-2 font-semibold text-white hover:bg-blue-500 cursor-pointer"
                    >
                        Save Changes
                    </button>

                </div>

            </form>
        </div>
    </div>
</template>
