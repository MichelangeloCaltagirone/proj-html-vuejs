<script>
    export default {
        data() {
            return {

            }
        }
    }
</script>

<template>

    <ul id="MainNavBarUl" class="pe-2">
        <li class="mainNavBarLi"><span class="hoverInfoSticky">Select Demo</span><i class="fa-solid fa-ruler-combined stickyIcon"></i></li>
        <li class="mainNavBarLi"><span class="hoverInfoSticky">Support Channel</span><i class="fa-solid fa-life-ring stickyIcon"></i></li>
        <li class="mainNavBarLi"><span class="hoverInfoSticky">Documentation</span><i class="fa-solid fa-book stickyIcon"></i></li>
        <li class="mainNavBarLi"><span class="hoverInfoSticky">Purchase Maxcoach</span><i class="fa-solid fa-cart-shopping stickyIcon"></i></li>
    </ul>

</template>

<style>
#MainNavBarUl {
    list-style-type: none;
    position: absolute;
    right: 0;
    top: 45%;
    margin: 0;
    padding: 5px;
    
    background-color: white;

}
.mainNavBarLi {
   display: flex;
   align-items: center;
   justify-content: flex-end;
   margin: 15px 0;

   .stickyIcon {
    font-size: 24px;
   }

    &:hover {
        .hoverInfoSticky {
            display: inline;
        }
    }
}

.hoverInfoSticky {
    font-size: 12px;
    font-weight: bold;
    color: white;
    background-color: black;
    border-radius: 5px;
    padding: 3px 5px;
    display: none;
    margin-right: 10px;
}

</style>