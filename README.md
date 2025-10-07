# tc-tac-toe
This is a game where user can play tic tac toe game
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        *{
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        .container{
            height: 500px;
            width: 500px;
            border: 2px solid black;
            margin: 100px auto;
            display: grid;
            grid-template-columns: repeat(3,1fr);
             grid-template-rows: repeat(3,1fr);
        }
        .items{
            background-color:white;
            border: 2px solid pink;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .items img{
            height: 100px;
        }
    </style>
</head>
<body>
    <section class="container">
       <div class="item1 items"></div>
       <div class="item2 items"></div>
       <div class="item3 items"></div>
       <div class="item4 items"></div>
       <div class="item5 items"></div>
       <div class="item6 items"></div>
       <div class="item7 items"></div>
       <div class="item8 items"></div>
       <div class="item9 items"></div>  
     </section>
     <script>
        let cross="https://www.nicepng.com/png/detail/12-123212_delete-tic-tac-toe-cross.png"
    let circle="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTv4_YfGiKWviHcItSV1I9LFdX45-Kc8HxmRDgnyj9giZ-nCVYYRZaJmpt3CC9AiL6-IEM&usqp=CAU"
        let divs=document.querySelectorAll('.items')
        let count=0;
        divs.forEach((el)=>
    {
        el.addEventListener('click',()=>
    {
        if(el.innerHTML==''){
            if(count%2==0)
        {
            el.innerHTML=`<img src=${cross}>`
            count++;
        }
        else{
            el.innerHTML=`<img src=${circle}>`
            count++;
        }
        }
    })
    })
    </script>
</body>
</html>
