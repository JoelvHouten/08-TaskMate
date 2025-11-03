<script setup lang="ts">
import { ref } from 'vue'

</script>

<template>
	<div class="container pt-4">
		<header class="taskmate-header text-center px-4 py-4 rounded">
			<div class="row justify-content-center">
				<div class="mb-3">
					<img src="../assets/images/taskmate-logo.png" alt="TaskMate logo" class="taskmate-logo mb-2">
				</div>

				<div class="col-md-10">
					<form class="d-flex justify-content-center align-items-center">
						<input
							type="text"
							class="form-control me-2 mb-2"
							placeholder="Vul hier uw taak in..."
						>
						<button type="button" class="btn btn-primary mb-2">Toevoegen</button>
					</form>
				</div>
			</div>
		</header>
	</div>
</template>

<style scoped>
.taskmate-header {
	background: linear-gradient(135deg, #1e293b, #0f172a);
	padding-top: 20px;
	padding-bottom: 20px;
	box-shadow: 0 5px 25px rgba(0, 0, 0, 0.4);
	border-radius: 12px;
}

.taskmate-logo {
	height: 125px;
}

.ui-block-color {
 	background: #0d1b2a;
}

.form-control {
	color: #e2e8f0 !important;
	background-color: #1e293b !important;
	border: 1px solid rgba(255, 255, 255, 0.1) !important;
	height: 42px;
	transition: all 0.2s ease;
}

.form-control:focus {
	box-shadow: 0 0 0 0.2rem rgba(209, 190, 140, 0.25) !important;
	border-color: #d1be8c !important;
}

input::placeholder {
  	color: #94a3b8 !important;
}
input:focus::placeholder {
 	 color: transparent !important;
}

.btn {
	--bs-btn-bg: #d1be8c !important;
	--bs-btn-border-color: #bfa973 !important;
	--bs-btn-hover-bg: #c4ac6d !important;
	--bs-btn-hover-border-color: #a9955d !important;
	--bs-btn-active-bg: #bfa973 !important;
	--bs-btn-active-border-color: #a78b55 !important;
	--bs-btn-disabled-bg: #4b5563 !important;
	--bs-btn-disabled-border-color: #6b7280 !important;
	color: #1e293b !important;
	font-weight: 500;
	transition: background-color 0.2s ease, border-color 0.2s ease;
}
</style>
