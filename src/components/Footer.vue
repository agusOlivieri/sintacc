<template>
    <footer class="bg-emerald-900 text-white py-10 mt-16">
      <div class="max-w-7xl mx-auto px-6 grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-8">
        
        <div>
          <h3 class="text-2xl font-bold mb-2">Sin TACC Market</h3>
          <p class="text-sm text-gray-300">
            Productos seleccionados sin T.A.C.C. para una vida más saludable.
          </p>
        </div>
  
        <div>
          <h4 class="text-lg font-semibold mb-2">Navegación</h4>
          <ul class="space-y-2 text-sm text-gray-300">
            <li><a href="#home" class="hover:text-white">Inicio</a></li>
            <li><a href="#products" class="hover:text-white">Productos</a></li>
          </ul>
        </div>
  
        <div>
          <h4 class="text-lg font-semibold mb-2">Contacto</h4>
          <ul class="text-sm text-gray-300 space-y-2">
            <li>Email: contacto@sintaccmarket.com</li>
            <li>Tel: +54 380 479-5484</li>
            <li>La Rioja, Argentina</li>
          </ul>
        </div>
  
        <div>
          <h4 class="text-lg font-semibold mb-2">Síguenos</h4>
          <div class="flex gap-4 text-white text-xl">
            <a href="#" class="hover:text-gray-300"><i class="pi pi-facebook"></i></a>
            <a href="https://www.instagram.com/deliciassintacc.lr/" class="hover:text-gray-300" target="_blank" rel="noopener noreferrer" ><i class="pi pi-instagram"></i></a>
          </div>
        </div>
  
      </div>
  
      <div class="border-t border-emerald-800 mt-10 pt-6 text-center text-sm text-gray-400">
        © {{ new Date().getFullYear() }} Sin TACC Market. Todos los derechos reservados.
      </div>
    </footer>
  </template>
  