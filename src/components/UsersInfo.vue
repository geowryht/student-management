<script>

</script>

<template>
    <div class="fixed inset-0 z-50 flex items-center justify-center bg-black/50">
        <div class="bg-white rounded-2xl shadow-xl w-[500px] max-w-3xl p-8">
            <div class="flex justify-center items-center mb-6">
                <h1 class="text-lg text-blue-500 font-bold uppercase ">User's Information</h1>
            </div>

            <form class="flex flex-col gap-5">
                <div class="flex justify-between gap-2 border-b border-gray-300 pb-1">
                    <p class="block mb-2 font-medium"> Id # </p>
                    <p class="block mb-2 font-medium"> Role </p>
                    <p class="block mb-2 font-medium"> Name </p>
                    <p class="block mb-2 font-medium"> Status </p>


                </div>



                <div class="flex justify-end gap-3 pt-3">
                    <button type="button"
                        class="px-5 py-2 border border-gray-300 bg-blue-500 text-white rounded-lg hover:bg-red-500">
                        Cancel
                    </button>


                </div>
            </form>
        </div>
    </div>

</template>