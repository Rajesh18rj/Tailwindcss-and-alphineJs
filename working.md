# 1

flex kudutha , antha container la irukathulam straight line ku vanthuduthu.. 

for example 

a
b

ipdi thani thaniya irukunaa.. flex kuduthathum

a b 

ipdi aagiduthu.. 

------------------------------------------------------------------------------------------------------------------------
items-center

now <flex item-center> nu kuduthathum, hight wise la center ku varuthu.. 

then 
  <flex justify-center
nu kuduthaa, 

height wise center ku pogama , width wise top of the center ku poguthu.. 

then
   <flex justify-center items-center>
nu kuduthaa, width oda center of the center poguthu.. 

< flex items-center justify-between>
intha mari kudutha items laam height wise center poi.. 
div kulla ippo rendu content iruku ..

 onnu <p>Awesome</p>
 innonu <p> Navigation </p>

intha mari iruntha rendum height wise center poi, onnu right corner , another one left corner pogiduthu.. 

lets come to nav section

<nav>
    <ul class="flex items-center ">
        <li> <a class="p-4 hover:bg-gray-700 rounded-lg" href="">Home</a> </li>
        <li><a class="p-4 hover:bg-gray-700 rounded-lg" href="">Create Post</a></li>
        <li><a class="p-4 hover:bg-gray-700 rounded-lg" href="">Bart</a></li>

    </ul>
</nav>

intha mari ovoru list ku thani thaniya class yeluthurathuku bathila, 

<nav>
    <ul class="flex items-center [&>li>a]:p-4 [&>li>a]:hover:bg-gray-700 [&>li>a]:rounded-lg ">
        <li> <a  href="">Home</a> </li>
        <li><a  href="">Create Post</a></li>
        <li><a  href="">Bart</a></li>

    </ul>
</nav>
 ipdi yeluthalam.. 

         then itha inga yelutha venam style tag kulla yeluthanum nu nenacha 

<style type="text/tailwindcss">
    .navitems {
        @apply [&>li>a]:p-4 [&>li>a]:hover:bg-gray-700 [&>li>a]:rounded-lg
    }
</style>

intha mari styles la yelutha athoda name ah class la kudukalam 
<nav>
    <ul class="flex items-center navitems ">                 #we give that name (navitems)
        <li> <a  href="">Home</a> </li>
        <li><a  href="">Create Post</a></li>
        <li><a  href="">' Bart</a></li>

    </ul>
</nav>

ipdi kuduthalum wrk aaagumm.. 

intha style ah innum kooda short panlam.. 

<style type="text/tailwindcss">
    .navitems>li>a {
        @apply p-4 hover:bg-gray-700 rounded-lg
    }
</style>
intha maari.. 

# 2

block
nu kuduthom naa , antha div kulla irukathu oru block ah aagidum.. 

then intha h1 tag ku predifend ah style la code yeluthalam ..            <h1> Awesome photos and Captions</h1>

h1 {
font-size: 4rem;
line-height: 1.2;
font-weight: bold;
margin-bottom: 1rem;
}

then eppolam h1 tag use panromo appolam ithu apply aagidum.. 

here we declare button class..<a class="button" href="">Get Started</a>

we write the design for this in style tag

.button {
display: inline-flex;
flex-wrap: wrap;
align-items: center;
justify-content: center;
flex-shrink: 0;
text-align: center;
border-radius: 0.5rem;
cursor: pointer;
padding: 0 1rem;
padding-left: 1rem;
min-height: 3.3rem;
font-weight: 600;
box-shadow: 0.4px 3px rgba(0,0,0,0.1);
transition-property: transform;
transition-duration: .2s;
color: white;
background-color: var(--primary);
}

.button:hover {
background-color: var(--primary-hover);
}

.button:active {
    transform: scale(0.95);
}

we give var primary for background-color and button hover bg color
so assign the value for this in top of the style tag

    :root {
    --primary: rgb(88, 40, 244);
    --primary-hover: rgb(69, 29, 200);
    }

then we are going to add bg image in class 

    bg-[url('...')]

then we want to change the font for heading 

so go to google fonts 

copy and paste emb code in header
<link href="https://fonts.googleapis.com/css2?family=Bona+Nova+SC:ital,wght@0,400;0,700;1,400&family=Lora:ital,wght@0,400..700;1,400..700&family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap" rel="stylesheet">

then add this font family in h1
    h1 {
    font-size: 4rem;
    line-height: 1.2;
    font-weight: bold;
    margin-bottom: 1rem;
    font-family: "Lora", serif;

just like this 

then title pakkathula icon iruntha nalla irukum .. so title tag ku keela itha kudukka porom 
<link rel="shortcut icon" type="image/png" href="https://img.icons8.com/small/64/ffffff/handshake-heart.png">
(intha icon image already namma use pannathu than.. )

