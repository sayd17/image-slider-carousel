<script>
    let name = 'Yoshi';
    let beltColor = 'black';

    const handleClick = () => {
        beltColor = 'orange';
        // beltColor = document.getElementById('updateColor').value;
    }

    const handleInput = (e) => {
        beltColor = e.target.value;
    }

</script>

<div>
    <h1>Hello {name}!</h1>
    <p>{beltColor}</p>
    <button on:click={handleClick}>update belt color</button>
    <input type="text" on:input={handleInput} value={beltColor} id="updateColor"/>
</div>