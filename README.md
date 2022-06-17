# Hello world
## Hello
ssssadasdasdasd
**sasdaasdasdsdsdasd**
*sasdasdasd*
list:
* asdasdasd
* asddsasda
 *sdasdasd
 
 ```javasript
 $("#activity").hide();
const types = ["education", "recreational", "social", "diy", "charity", "cooking", "relaxation", "music", "busywork"];

$(document).ready(function(){
    $.each(types, function (index, type) { 
         $("#types").append(`
            <label for="${type}">${type.toUpperCase()}</label>
            <input type="radio" id="${type}" name="type" value="${type}">
         `);
    });

    $("#rndActBtn").click(function() { 
        let params = $("#filters").serialize();
        console.log(params);
        $.ajax({
            url: `https://www.boredapi.com/api/activity/?${params}`,
            success: function (response) {
                console.log(response);
                $("#activity").html(`
                    <p>Activity: ${response.activity}</p>
                    <p>Price: ${response.price}</p>
                    <p>Type: ${response.type}</p>
                `);
            }
        });
        $("#activity").show();
        $("#rndActBtn").html("Randimize Again")       
    });
});
```
https://github.com/
![](https://www.pngall.com/wp-content/uploads/2016/03/Cat-PNG-2.png)
