<script setup lang="ts"></script>
<template>
    <div class="profileimg">

        <div>
            <img src="/womanA.jpg" alt="Woman Pic" />
        </div>
        <div class="profileinfo"> 
            <h1>Tosin Shokumbi</h1>
            <p>Chartered Accountant, Digital skills Trainer, and Entrepreneur</p>
            <section>
                <button>Learn More</button>
            </section>
        </div>
    </div>
</template>

<style scoped>
.profileimg{
    display: flex;
    align-items: center;
    gap:60px
}
.profileinfo{
    flex: 1.5;
    padding: 1px;
    text-align: left;
}
h1 {
  font-size: 4rem;
}
button {
  background-color: black;
  color: white;
  padding: 5px 10px;
  border: none;
  border-radius: 5px;
  width: 400px;
  margin: 1.5rem auto;
  
}
</style>
