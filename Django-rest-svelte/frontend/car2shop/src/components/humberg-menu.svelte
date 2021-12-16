<div class="container" class:change={change} on:click="{() => change = !change}">
    <div class="bar1"></div>
    <div class="bar2"></div>
    <div class="bar3"></div>
  </div>
  
  <div class="sidenav closeNav flex flex-col justify-start items-center" class:openNav={change} >
    
    <a class="basis-1/5" href="#">About</a>
    <a class="basis-1/5" href="#">Services</a>
    <a class="basis-1/5" href="#">Clients</a>
    <a class="basis-2/5" href="#">Contact</a>
  </div>


  <script>
 let change=false;

  </script>
<style>
@tailwind base;
@tailwind components;
@tailwind utilities;
@media  (max-width:1023.5px)
{
    .container {
  display: inline-block;
  cursor: pointer;
}

 .bar2{
  width: 35px;
  height: 4px;
  background-color: white;
  margin: 6px 0;
  transition: 0.4s;
   
}
.bar1,.bar3 {
  width: 25px;
  height: 4px;
  background-color: white;
  margin: 6px 0;
  transition: 0.4s;
  margin-left:10px;

}
.change .bar1 {
  -webkit-transform: rotate(-45deg) translate(-9px, 6px);
  transform: rotate(-45deg) translate(-9px, 6px);
  width: 35px;
  margin-left:0px;
  background-color: white;

}

.change .bar2 {opacity: 0;}

.change .bar3 {
    background-color: white;
  -webkit-transform: rotate(45deg) translate(-8px, -8px);
  transform: rotate(45deg) translate(-8px, -8px);
  width: 35px;
  margin-left:0px;
  
}

.openNav
{
    width :250px !important;
}

.closeNav{
    width :0px;
}
.sidenav {
    margin-top:75px;
  height: 50%;
  width: 0;
  position: fixed;
  z-index: 10;
  top: 0;
  right: 0;
  background-color: white;
  overflow-x: hidden;
  transition: 0.5s;
  padding-top: 60px;
}

.sidenav a {
  
  text-decoration: none;
  font-size: 25px;
  color: #818181;
  display: block;
  transition: 0.3s;
}

.sidenav a:hover {
  color: #f1f1f1;
}





}

</style>