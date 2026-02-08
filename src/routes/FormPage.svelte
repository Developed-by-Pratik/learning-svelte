<script>
	let form_data = $state({
		name: '',
		gender: '',
		step: 1,
		error: ''
	});
</script>

<main>
	<p>Step : {form_data.step}</p>
	<p class="error">{form_data.error}</p>
	<p>Name : {form_data.name}</p>
	<p>Gender : {form_data.gender}</p>

	{#if form_data.step === 1}
		<div>
			<span>Enter Your Name : </span>
			<input type="text" bind:value={form_data.name} /> <br />
			<button
				onclick={() => {
					if (form_data.name !== '') {
						form_data.step += 1;
					} else {
						form_data.error = 'Your name is empty !';
					}
				}}>Next Step</button
			>
		</div>
	{:else if form_data.step === 2}
		<div>
			<span>Select Your gender : </span>
			<select bind:value={form_data.gender}>
				<option value="M">Male</option>
				<option value="F">Female</option>
				<option value="NA">Other</option>
			</select>
			<button
				onclick={() => {
					if (form_data.gender !== '') {
						form_data.step += 1;
					} else {
						form_data.error = 'Please select your gender !';
					}
				}}>Next Step</button
			>
		</div>
	{/if}
</main>

<style>
	.error {
		color: red;
		font-weight: bold;
	}
</style>
