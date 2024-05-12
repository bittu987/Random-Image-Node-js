
# Generate Random Image API

**Write code for API Creation**

```
    // Import express 
    const express = require('express');

    const server = express(); // Create server 
    const Port = 4040;


    function generateRandomImageUrl() {
        const width = 600; // Given image width
        const height = 500; // Given Image height
        const randomImageId = Math.floor(Math.random() * 1000); // Generate ID number
        return `https://picsum.photos/${width}/${height}?image=${randomImageId}`;
    }

    server.get('/randomImage',(req,res)=>{
    const imageURL = generateRandomImageUrl(); // generate Image URL
    
    res.json({
            imageLink : imageURL,
            message: "Success"
    })
    
    });



    server.listen(Port,()=> {
        console.log(`Server is running on http://localhost:${Port}`);
    })

```

### Successfully get API using PostMan 

