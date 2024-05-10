<template>
  <header class="flex justify-between border-b border-slate-300 px-10 py-8">
    <div class="flex items-center gap-4">
      <img src="/logo.png" alt="logo" class="w-10" />
      <div>
        <h2 class="text-xl font-bold uppercase">Sneakers SHOP</h2>
        <p class="text-slate-400">Магазин лучших кроссовок</p>
      </div>
    </div>

    <nav class="my-auto">
      <ul class="w-full flex items-center gap-8 text-slate-500">
        <li class="cursor-pointer hover:text-black">
          <a href="#" class="flex items-center gap-2"
            ><img src="/cart.svg" alt="cart" /> <span>1025 руб</span></a
          >
        </li>
        <li class="cursor-pointer hover:text-black">
          <a href="#" class="flex items-center gap-2"
            ><img src="/heart.svg" alt="favorites" /> <span>Избранное</span>
          </a>
        </li>
        <li class="cursor-pointer hover:text-black">
          <a href="#" class="flex items-center gap-2"
            ><img src="/profile.svg" alt="profile" /> <span>Профиль</span></a
          >
        </li>
      </ul>
    </nav>
  </header>
</template>
