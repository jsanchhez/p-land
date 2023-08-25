<script>
let wordSearch = "";
let textSearch = "";
let replaceText = "";
let replaceWord = "";
function SSearch (){
if(textSearch.toLowerCase().includes(wordSearch.toLowerCase())){
    alert("Match Found")
}else{
    alert("No Match Found")
}
}
function cooking (){
    let newString = replaceText.replaceAll(replaceWord, "REDACTED");
    alert(newString);

}

//key indexed array
let products = new Map();
products.set("apple", 0.99);
products.set("orange", 1.99);
products.set("banana", 0.59);

</script>
<h1 class="text-3xl font-bold text-gray-900">Random Javascript Exercises</h1>

<form on:submit|preventDefault={SSearch}>
    <label for="wordSearch">Search Here:</label><br>
    <input class="text-black mb-4" type="text" id="search" bind:value={wordSearch}><br>
    <label for="textSearch">Text to search:</label><br>
    <input class="text-black mb-4" type="text" id="text" bind:value={textSearch}><br>
    <input type="submit" value="Submit" class="mt-2 bg-green-200 text-white px-4 py-2 border-none cursor-pointer">
  </form>

  <h1 class="text-3xl font-bold text-gray-900">Random text</h1>
  <div class="text-3xl font-bold text-gray-900">
    <p></p>
  </div>



<form on:submit|preventDefault={cooking}>
<label for="replaceText">REPLACEOMATIC</label><br>
<p>enter the text you would like the word replaced from</p> <br>
<input class="text-black mb-4" type="text" id="replaceText" bind:value={replaceText}><br>
<label for="replaceWord">Replace Word:</label><br>
<input class="text-black mb-4" type="text" id="replaceWord" bind:value={replaceWord}><br>
<input type="submit" value="Submit" class="mt-2 bg-green-200 text-white px-4 py-2 border-none cursor-pointer">
</form>

cont l,


