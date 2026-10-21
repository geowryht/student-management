<script>

</script>

<template>
    <div class="fixed inset-0 z-50 flex items-center justify-center bg-black/50">
        <div class="bg-white rounded-2xl shadow-xl w-[500px] max-w-3xl p-8">
            <div class="flex justify-center items-center mb-6">
                <h2 class="text-lg text-red-500 font-bold uppercase ">Add new student</h2>

            </div>

            <form class="flex flex-col gap-5">
                <div>
                    <label class="block mb-2 font-medium"> Name * </label>

                    <input type="text" placeholder="Full Name" class="w-full border border-zinc-400  outline-blue-600 rounded-lg px-4 py-3" />
                </div>

                <div>
                    <label class="block mb-2 font-medium"> Address * </label>

                    <input type="text" placeholder="Complete Address" class="w-full border border-zinc-400  outline-blue-600 rounded-lg px-4 py-3" />
                </div>

                <div class="flex gap-5">
                    <div class="flex-1">
                        <label class="block mb-2 font-medium"> Age * </label>

                       <input type="number" placeholder="eg. 18" class="w-full border border-zinc-400  outline-blue-600 rounded-lg px-4 py-3" />
                    </div>

                    <div class="flex-1">
                        <label class="block mb-2 font-medium"> Contact Number * </label>

                       <input type="number" placeholder="Phone Number" class="w-full border border-zinc-400  outline-blue-600 rounded-lg px-4 py-3" />
                    </div>

                </div>

                

                <div class="flex justify-end gap-3 pt-3">
                    <button type="button" class="px-5 py-2 border border-gray-300 rounded-lg hover:bg-gray-100">
                        Cancel
                    </button>

                    <button type="submit" class="px-5 py-2 bg-blue-700 text-white rounded-lg hover:bg-blue-800">
                        Save
                    </button>
                </div>
            </form>
        </div>
    </div>

</template>