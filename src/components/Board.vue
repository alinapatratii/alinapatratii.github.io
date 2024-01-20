<script setup>
	import Column from './Column.vue';

	defineProps({
		columns: {
            type: Array,
			required: true
		}
	});
</script>

<template>
	<div class="container">
		<button type="button" class="btn btn-info btn-lg" data-toggle="modal" data-target="#myModal">Open Modal</button>
		<div id="myModal" class="modal fade" role="dialog">
			<div class="modal-dialog">
			<!-- Modal content-->
				<div class="modal-content">
					<div class="modal-header">
						<button type="button" class="close" data-dismiss="modal">&times;</button>
						<h4 class="modal-title">Modal Header</h4>
					</div>
					<div class="modal-body">
						<p>Some text in the modal.</p>
					</div>
					<div class="modal-footer">
						<button type="button" class="btn btn-default" data-dismiss="modal">Close</button>
					</div>
				</div>
			</div>
		</div>
		<div class="row">
			<div v-for="column in columns" class="col-12 col-md-6 col-lg-4">
                <Column :key="column.id" :column="column" />
			</div>
		</div>
	</div>
</template>
