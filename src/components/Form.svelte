<script>
    let product = { id: '', name: '', description: '', categoria: '', imagesUrl: ''};

	const enviarSubmit = e => {
		console.log(product);
	}
</script>

<div class="w-full max-w-xs mx-auto my-4">
    <form class="bg-white rounded-lg shadow-xl px-8 pt-6 pb-8 mb-4" on:submit|preventDefault={enviarSubmit}>
		<div class="mb-4 text-gray-700">
            <label class="block text-sm font-bold mb-2 text-center">Producto</label>
			<input
                class="shadow appearance-none border rounded w-full py-2 px-3  leading-tight focus:outline-none focus:shadow-outline"
                bind:value={product.name}
                id="product-name"
                type="text"
                placeholder="product name"
            />
		</div>
        <div class="mb-4 text-gray-700">
            <label class="block text-sm font-bold mb-2 text-center">Descripción</label>
            <textarea
                class="w-full max-w-xs"
                bind:value={product.description}
                id="product-description"
                rows="3"
            />
		</div>
        <div class="mb-4 text-gray-700">
            <label class="block text-sm font-bold mb-2 text-center">Imagen</label>
            <input
                class="placeholder-indigo-500 shadow appearance-none border rounded w-full py-2 px-3 leading-tight focus:outline-none focus:shadow-outline"
                bind:value={product.imageUrl}
                type="url"
                id="product-image-url"
                placeholder="https://jpweb.com"
            />
		</div>
        <div class="mb-4 text-gray-700" >
            <label class="block text-sm font-bold mb-2 text-center">Categoria</label>
            <select
                class="block appearance-none w-full bg-gray-200 border border-gray-200 py-3 px-4 pr-8 rounded leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
                bind:value={product.categoria}
                id="category">
				<option value="laptops">Laptops</option>
				<option value="perifericos">Perifericos</option>
				<option value="servidores">Servidores</option>
			</select>
		</div>
		<div class="mb-4 flex">
			<button class="justify-center bg-indigo-500 mx-auto hover:bg-blue-700 text-white font-semibold py-2 px-4 border  hover:border-transparent rounded">Save Product</button>
		</div>
	</form>
</div>