<style src="./preview.css"></style>
<script src="./preview.js"></script>

<template>
	<div id="lorems-preview-component">
		<div id="lorems-preview-edit">
			<button @click="editLorem()">Edit</button>
		</div>
		<div id="lorems-preview-content">
			<p><label class="preview-label">Version:</label> {{ store.selectedLorem.iteration }}</p>
			<p>
				<label class="preview-label">Name:</label>
				{{ store.selectedLorem.firstname }} {{ store.selectedLorem.lastname }}
			</p>
			<p><label class="preview-label">Username:</label> {{ store.selectedLorem.username }}</p>
			<p><label class="preview-label">Email:</label> {{ store.selectedLorem.email }}</p>
			<p><label class="preview-label">Rating:</label> {{ store.selectedLorem.rating }}</p>
			<p><label class="preview-label">Species:</label> {{ store.selectedLorem.species }}</p>
			<p><label class="preview-label">Created&nbsp;At:</label>{{ momentDate(store.selectedLorem.createdAt) }}</p>
			<p style="width: 400px;"><label class="preview-label">Description:</label>&nbsp;
				{{ store.selectedLorem.description }}</p>
		</div>
		<Versions/>
	</div>

</template>
