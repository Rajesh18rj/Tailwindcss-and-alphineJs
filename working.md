# 1

flex kudutha , antha container la irukathulam straight line ku vanthuduthu.. 

for example 

a
b

ipdi thani thaniya irukunaa.. flex kuduthathum

a b 

ipdi aagiduthu.. 

-----------------------------------------------------------------------------------------------------------------------------------------------
items-center


now <flex item-center> nu kuduthathum, height wise la center ku varuthu.. 

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

# 3

we need a card so we define that in style 

    .card {
    display: flex;
    flex-direction: column;
    overflow: hidden;
    position: relative;
    border-radius: 1rem;
    box-shadow: 0 10px 15px -3px rgba(0,0,0,0.1);
    margin-bottom: 2rem;
    background-color: white;
    padding-bottom: 1rem;
    }
then we use that in article tag

    <article class="card h-36">Post</article>

<h3 class="text-lg font-bold w-[50%] truncate">Little Jedi is the one who is dump and shit</h3>

w-[50%] truncate
enna pannum naa.. card oda width 50 % mela aanathum balance words ah ... (dot vachu) kaatum 

# 4 side bar

we also define the h2 properties in styles

    h2 {
    font-size: 1.5rem;
    line-height: 2rem;
    font-weight: bold;
    margin-bottom: 0.75rem;
    }

then we are creating hoverlist attribute 

    <ul class="hoverlist">
and we define that in style

    .hoverlist>* {
    @apply hover:bg-gray-100 rounded-md transition duration-150;
    }
    .hoverlist>*>a {
    @apply p-2 block;
    }

# 5

lets add the alphine js to our code , first insert the cdn link in end of the header just like we did it for tailwindcss 

    <li x-data class="relative">

x-data means this element is talking to alphine.js

    <!--Right Side-->
            <nav>
                <ul class="flex items-center navitems">
                    <li><a href="">Home</a></li>
                    <li><a href="">Create Post</a></li>
                    <li x-data="{ dropdownOpen: false}" class="relative">
                        <a @click="dropdownOpen = !dropdownOpen" @click.away="dropdownOpen = false" class="cursor-pointer select-none" >
                            <img class="h-8 rounded-full object-cover bg-teal-200" src="https://img.icons8.com/doodle/96/bart-simpson.png" alt="bart-simpson"/>
                            Bart
                            <img x-bind:class="dropdownOpen ? 'rotate-180 duration-300' : '' " class="w-4 " src="https://img.icons8.com/small/64/777777/expand-arrow.png" alt="expand-arrow"/>
                        </a>
                        <div x-show="dropdownOpen" x-cloak class="absolute right-0 bg-white text-black shadow rounded-lg w-40 p-2 z-20 "
                        x-transition:enter="duration-300 ease-out"
                        x-transition:enter-start="opacity-0 -translate-y-5 scale-90"
                        x-transition:enter-end="opacity-100 translate-y-0 scale-100"

                        >
                            <ul class="hoverlist [&>li>a]:justify-end">
                                <li><a href="">My Profile</a></li>
                                <li><a href="">Log Out</a></li>
                            </ul>
                        </div>
                    </li>

                </ul>
            </nav>

# 6 

responsive header 

firstu mobile view ku responsive ah iruka mari create panna porom..

  <mobileicon >
    <a class="h-12 w-12 flex items-center justify-center cursor-pointer hover:bg-gray-700 rounded-lg">
        <img class="w-6 h-6" src="https://img.icons8.com/small/64/ffffff/menu.png" alt="">
    </a>
</mobileicon>

then ,mobile view ku varum bothu oru sila vishayam hide pannanum
  <!--Right Side-->
    <nav class="hidden md:block">

this means nav bar la right ku mble view la vantha home, create Post, Bart elllam hidden aagirum

learn about more this in tailwind css docs -> customizing screens 

now enna panna porom na... laptop or desktop screen la antha sandwidch icon ah hide panna porom..
<mobileicon class="md:hidden">
just like this 

now ipo enna panna porom naa antha sandwitch icon ah click pannathum.. home , create post and bart ellamey open aaganum 

now come to header tag lets initialize alphine.js 

<body class="bg-gray-100">
        <header x-data="{ mobilenavOpen: false }"  class="flex items-center justify-between px-8 bg-gray-800 h-20 text-white sticky top-0 z-50">
            <!--Logo(Left Side)-->
            <logo>
                <a class="flex items-center gap-1" href="">
                    <img class="h-8 -mt-1" src="https://img.icons8.com/small/64/ffffff/handshake-heart.png" alt="handshake-heart"/>
                    <span>Awesome</span>
                </a>
            </logo>

            <mobileicon class="md:hidden">
                <a @click="mobilenavOpen = !mobilenavOpen" class="h-12 w-12 flex items-center justify-center cursor-pointer hover:bg-gray-700 rounded-lg">
                    <img class="w-6 h-6" src="https://img.icons8.com/small/64/ffffff/menu.png" alt="">
                </a>
            </mobileicon>

            <!--Right Side-->
            <nav x-show="mobilenavOpen" class=" md:block">

now when i click hamburger icon .. it opens home , create Posts, Bart 
 
now ellamey those things (home , create Posts, Bart ) horizontal ah iruku namma vertical ah matha porom.. 

 <mobileicon class="md:hidden">
    <a @click="mobilenavOpen = !mobilenavOpen" class="h-12 w-12 flex items-center justify-center cursor-pointer hover:bg-gray-700 rounded-lg">
        <img x-show="!mobilenavOpen" class="w-6 h-6 select-none" src="https://img.icons8.com/small/64/ffffff/menu.png" alt="">
        <img x-show="mobilenavOpen" x-cloak class="w-6 h-6 select-none" src="https://img.icons8.com/small/64/ffffff/delete-sign.png" alt="">
    </a>
</mobileicon>

namma inga menu icon ku keela cancel icon add pannirukom.. then athuku alphine js vachu code um yeluthirukom.. 
if menu va click panna enna nadakanum.. cancel ah click panna enna nadakum nu define pannirukom

