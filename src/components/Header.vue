<script setup>
///////////////////////////////////////////////
// IDs to be used for the respective DOM elements in the template
///////////////////////////////////////////////

const BUTTON_TOGGLE_MODAL_ID = 'buttonToggleModal' // for the button that opens the modal

///////////////////////////////////////////////
// Your implementation below
///////////////////////////////////////////////

defineProps({
    title: {
        type: String,
        required: true
    },
    /* MODAL_ID: {
        type: String,
        required: true
    } */
});
</script>

<template>
    <nav class="navbar bg-light">
        <div class="container-fluid">
            <!-- Logo and title of the Kanban board -->
            <span class="navbar-brand mb-0 h1">
                <img src="../assets/logo.svg" alt="Logo" width="24" height="24" class="d-inline-block align-text-top">
                {{ title }}
            </span>

            <!-- TODO: button -->
            <button type="button" class="btn btn-outline-primary" data-toggle=".modal" data-target="#modalRoot" :id="BUTTON_TOGGLE_MODAL_ID">Create new task</button>
            <button type="button" class="btn btn-primary" data-toggle="collapse" data-target="#exampleModalLong">
                Launch demo modal
            </button>
            <div class="modal fade" id="exampleModalLong" tabindex="-1" role="dialog" aria-labelledby="exampleModalLongTitle" aria-hidden="true">
                <div class="modal-dialog" role="document">
                    <div class="modal-content">
                        <div class="modal-header">
                            <h5 class="modal-title" id="exampleModalLongTitle">Modal title</h5>
                            <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                            <span aria-hidden="true">&times;</span>
                            </button>
                        </div>
                        <div class="modal-body">
                            ...
                        </div>
                        <div class="modal-footer">
                            <button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
                            <button type="button" class="btn btn-primary">Save changes</button>
                        </div>
                        </div>
                    </div>
                </div>
        </div>
    </nav>
</template>