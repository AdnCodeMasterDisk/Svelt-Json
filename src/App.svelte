
  <script>
    // @ts-nocheck
    
      import '../src/assets/style.css'
      import dataJson from './assets/data.json'
    
      //on line read
      let arrayJson = []
      let linkJson = 'https://raw.githubusercontent.com/AdnCodeMasterDisk/jsontest/main/array.json'
    
      const readJson = async() => {
        const data = await
        fetch(linkJson)
        const json = await data.json()
        arrayJson = json
      }
    
      //inicializamos la funcion
      readJson()
     
    </script>
    
    <h3>From local Json </h3>
    <!--Local Json Read-->
    {#each dataJson as element, i}
            <p>
                {i} - {element.username} - {element.email}
            </p>
    {/each}
    
    <h3>From Internet Json </h3>
    <!-- on line read-->
    {#each arrayJson as array, i}
            <p>
                {i} - {array.username} - {array.email}
            </p>
    {/each}
    
    