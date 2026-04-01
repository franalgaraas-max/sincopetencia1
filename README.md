<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>Sincompetencia | Indumentaria Deportiva</title>
    <!-- Font Awesome 6 -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,400;14..32,500;14..32,600;14..32,700;14..32,800&family=Anton&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f4f4f4;
            color: #111;
            line-height: 1.5;
        }
        .top-bar {
            background-color: #000;
            color: #fff;
            padding: 8px 20px;
            font-size: 0.85rem;
            text-align: center;
        }
        .top-bar i {
            margin: 0 4px;
        }
        header {
            background: #fff;
            padding: 15px 5%;
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
            border-bottom: 3px solid #00ff99;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        .logo h1 {
            font-family: 'Anton', sans-serif;
            font-size: 2rem;
            letter-spacing: 2px;
            background: linear-gradient(135deg, #000 60%, #00ff99);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        .logo p {
            font-size: 0.75rem;
            color: #555;
        }
        .nav-icons {
            display: flex;
            gap: 25px;
            align-items: center;
        }
        .nav-icons a {
            color: #111;
            font-size: 1.5rem;
            transition: 0.2s;
        }
        .nav-icons a:hover {
            color: #00cc77;
        }
        .cart-icon {
            position: relative;
            cursor: pointer;
        }
        .cart-count {
            position: absolute;
            top: -10px;
            right: -12px;
            background: #00ff99;
            color: #000;
            font-size: 0.7rem;
            font-weight: bold;
            border-radius: 50%;
            width: 20px;
            height: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .hero {
            background: linear-gradient(97deg, #0a0a0a 30%, #1a1a1a 100%);
            color: white;
            padding: 40px 5%;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            gap: 30px;
        }
        .hero-info {
            flex: 2;
            min-width: 240px;
        }
        .hero-info h2 {
            font-size: 2.2rem;
            font-weight: 800;
        }
        .hero-info h2 span {
            color: #00ff99;
        }
        .stats {
            display: flex;
            gap: 30px;
            margin: 20px 0;
            font-size: 0.9rem;
        }
        .stats div i {
            margin-right: 8px;
            color: #00ff99;
        }
        .hero-badge {
            background: #00ff99;
            color: #000;
            display: inline-block;
            padding: 5px 12px;
            border-radius: 30px;
            font-weight: bold;
            font-size: 0.8rem;
            margin-top: 15px;
        }
        .hero-links {
            flex: 1;
            background: rgba(255,255,255,0.05);
            border-radius: 20px;
            padding: 20px;
            backdrop-filter: blur(4px);
        }
        .hero-links h3 {
            font-size: 1.2rem;
            margin-bottom: 15px;
            border-left: 4px solid #00ff99;
            padding-left: 10px;
        }
        .social-buttons {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin-top: 15px;
        }
        .social-buttons a {
            background: #222;
            padding: 8px 14px;
            border-radius: 40px;
            color: white;
            text-decoration: none;
            font-size: 0.9rem;
            transition: 0.2s;
        }
        .social-buttons a i {
            margin-right: 8px;
        }
        .social-buttons a:hover {
            background: #00ff99;
            color: black;
        }
        .team-badges {
            background: white;
            padding: 12px 5%;
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            border-bottom: 1px solid #ddd;
            font-weight: 600;
        }
        .team-badges span {
            background: #eee;
            padding: 5px 15px;
            border-radius: 40px;
            font-size: 0.85rem;
        }
        .products-section {
            padding: 40px 5%;
        }
        .section-title {
            font-size: 1.8rem;
            margin-bottom: 30px;
            font-weight: 800;
            display: flex;
            justify-content: space-between;
            align-items: baseline;
            flex-wrap: wrap;
        }
        .price-tag {
            background: #00ff99;
            padding: 8px 20px;
            border-radius: 40px;
            font-size: 1rem;
            font-weight: bold;
        }
        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
            gap: 30px;
            margin-bottom: 40px;
        }
        .product-card {
            background: white;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 8px 20px rgba(0,0,0,0.05);
            transition: transform 0.2s, box-shadow 0.2s;
        }
        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 12px 25px rgba(0,0,0,0.1);
        }
        .product-img {
            width: 100%;
            aspect-ratio: 1 / 1;
            background-color: #f0f0f0;
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            font-weight: bold;
            color: white;
            text-shadow: 0 0 5px rgba(0,0,0,0.5);
        }
        .product-info {
            padding: 18px;
        }
        .product-name {
            font-weight: 700;
            font-size: 1.1rem;
            margin-bottom: 5px;
        }
        .product-sizes {
            font-size: 0.75rem;
            color: #666;
            margin-bottom: 8px;
        }
        .product-price {
            font-weight: 800;
            color: #00aa66;
            font-size: 1.2rem;
            margin: 10px 0;
        }
        .add-to-cart {
            background: black;
            color: white;
            border: none;
            width: 100%;
            padding: 10px;
            border-radius: 40px;
            font-weight: 600;
            cursor: pointer;
            transition: 0.2s;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }
        .add-to-cart:hover {
            background: #00ff99;
            color: black;
        }
        .pagination {
            display: flex;
            justify-content: center;
            gap: 12px;
            margin-top: 20px;
            flex-wrap: wrap;
        }
        .page-btn {
            background: white;
            border: 1px solid #ccc;
            padding: 8px 16px;
            border-radius: 40px;
            cursor: pointer;
            font-weight: 600;
        }
        .page-btn.active {
            background: black;
            color: white;
            border-color: black;
        }
        .cart-modal {
            position: fixed;
            top: 0;
            right: -100%;
            width: 100%;
            max-width: 450px;
            height: 100%;
            background: white;
            box-shadow: -5px 0 20px rgba(0,0,0,0.2);
            z-index: 1000;
            transition: 0.3s;
            display: flex;
            flex-direction: column;
            padding: 20px;
        }
        .cart-modal.open {
            right: 0;
        }
        .cart-header {
            display: flex;
            justify-content: space-between;
            font-size: 1.5rem;
            font-weight: bold;
            border-bottom: 2px solid #eee;
            padding-bottom: 15px;
        }
        .cart-items {
            flex: 1;
            overflow-y: auto;
            margin: 20px 0;
        }
        .cart-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 1px solid #eee;
            padding: 12px 0;
        }
        .cart-item-info {
            flex: 2;
        }
        .cart-item-name {
            font-weight: 600;
        }
        .cart-item-price {
            font-size: 0.9rem;
        }
        .cart-item-qty {
            display: flex;
            align-items: center;
            gap: 8px;
        }
        .cart-item-qty button {
            background: #eee;
            border: none;
            width: 28px;
            height: 28px;
            border-radius: 50%;
            cursor: pointer;
        }
        .cart-total {
            border-top: 2px solid #ddd;
            padding-top: 15px;
            font-weight: 800;
            font-size: 1.2rem;
            text-align: right;
        }
        .checkout-btn {
            background: #00cc77;
            border: none;
            padding: 15px;
            font-weight: bold;
            border-radius: 40px;
            margin-top: 15px;
            cursor: pointer;
            font-size: 1rem;
        }
        .close-cart {
            background: none;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
        }
        .overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.5);
            visibility: hidden;
            z-index: 999;
        }
        .overlay.active {
            visibility: visible;
        }
        footer {
            background: #000;
            color: #ccc;
            text-align: center;
            padding: 30px 5%;
            margin-top: 40px;
        }
        @media (max-width: 700px) {
            .hero-info h2 {
                font-size: 1.8rem;
            }
            .logo h1 {
                font-size: 1.5rem;
            }
        }
    </style>
</head>
<body>

<div class="top-bar">
    <i class="fas fa-truck"></i> Envíos a todo el país | <i class="fas fa-store"></i> Local en Rosario - Juan José Paso
</div>

<header>
    <div class="logo">
        <h1>SINCOMPETENCIA</h1>
        <p>Indumentaria deportiva · Ex dueños del Tío Salim</p>
    </div>
    <div class="nav-icons">
        <a href="https://www.instagram.com/Sincompetencia1" target="_blank"><i class="fab fa-instagram"></i></a>
        <div class="cart-icon" id="cartIcon">
            <i class="fas fa-shopping-cart"></i>
            <span class="cart-count" id="cartCount">0</span>
        </div>
    </div>
</header>

<section class="hero">
    <div class="hero-info">
        <h2>ROPA DE <span>FÚTBOL</span><br>AL MEJOR PRECIO</h2>
        <div class="stats">
            <div><i class="fas fa-newspaper"></i> 889 publicaciones</div>
            <div><i class="fas fa-users"></i> 6,342 seguidores</div>
            <div><i class="fas fa-user-plus"></i> 2,440 seguidos</div>
        </div>
        <p><i class="fas fa-map-marker-alt"></i> Rosario - Santa Fe | Puesto a la calle + Local</p>
        <div class="hero-badge">🏆 Líder en ropa de fútbol · Polirubro</div>
    </div>
    <div class="hero-links">
        <h3>CONTACTO DIRECTO</h3>
        <div class="social-buttons">
            <a href="https://wa.me/5491159669909?text=Hola!%20Quiero%20comprar%20en%20Sincompetencia" target="_blank"><i class="fab fa-whatsapp"></i> WhatsApp</a>
            <a href="https://www.instagram.com/Sincompetencia1" target="_blank"><i class="fab fa-instagram"></i> Instagram</a>
            <a href="#" target="_blank"><i class="fab fa-tiktok"></i> TikTok</a>
            <a href="#" target="_blank"><i class="fab fa-facebook"></i> Facebook</a>
            <a href="#" target="_blank"><i class="fas fa-map-pin"></i> Ubicación</a>
        </div>
        <div style="margin-top: 20px; font-size:0.85rem">
            <i class="fas fa-link"></i> <a href="http://www.atom.bio/sincompetencia1" style="color:#00ff99;" target="_blank">atom.bio/sincompetencia1</a>
        </div>
    </div>
</section>

<div class="team-badges">
    <span>⚽ Aldosivi 🇦🇷</span>
    <span>⚽ Platense 🇧🇷</span>
    <span>⚽ E D L P 🇨🇴</span>
    <span>⚽ RC 🇳🇬</span>
    <span>⚽ Estudiantes</span>
    <span>⚽ Chicago</span>
    <span>🔥 EL LOCAL MÁS PICANTE 🔥</span>
</div>

<section class="products-section">
    <div class="section-title">
        <span>🔥 TODAS LAS REMERAS 🔥</span>
        <div class="price-tag">💰 $22.000 ARS c/u</div>
    </div>
    <div class="product-grid" id="productGrid"></div>
    <div class="pagination" id="paginationControls"></div>
</section>

<footer>
    <p>Sincompetencia - Indumentaria deportiva líder en Rosario | Envíos a todo el país 🇦🇷</p>
    <p style="margin-top: 10px;">📍 Juan José Paso - Rosario | Ex dueños del Tío Salim, empresa familiar reconocida</p>
    <p style="margin-top: 15px;">⭐ Seguinos en @Sincompetencia1 ⭐</p>
</footer>

<!-- Modal carrito -->
<div class="overlay" id="overlay"></div>
<div class="cart-modal" id="cartModal">
    <div class="cart-header">
        <span>🛒 Mi Carrito</span>
        <button class="close-cart" id="closeCartBtn"><i class="fas fa-times"></i></button>
    </div>
    <div class="cart-items" id="cartItemsList">
        <p style="text-align:center;">Carrito vacío</p>
    </div>
    <div class="cart-total" id="cartTotal">Total: $0</div>
    <button class="checkout-btn" id="checkoutBtn">📲 FINALIZAR COMPRA POR WHATSAPP</button>
</div>

<script>
    // =======================================================
    // 1. IMÁGENES DESDE GOOGLE DRIVE (IDs reales)
    // =======================================================
    // IDs de las imágenes de tu carpeta:
    // IMG-20260401-WA0004.jpg, IMG-20260401-WA0005.jpg, etc.
    const imagenesIDs = [
        "1vBsc1ZJs07-0HGF1HxNAQpIjBg87Sk-a",  // IMG-20260401-WA0004.jpg
        "1nNWHN-hiKb5N7adxogBSWYvyD6v-E4Pc",  // IMG-20260401-WA0005.jpg
        "1rFv0oF01t0m6WTR2uy4UDSK4yaZvyNU-",  // IMG-20260401-WA0006.jpg
        "1eOj-_vIDHGWCFxc-6wtjKzCb3EQ9K6Z3",  // IMG-20260401-WA0007.jpg
        "1mv7bYJ4I_YenHmJxR44jPCn05J6ZP_7S",  // IMG-20260401-WA0008.jpg
        "1dovbOJvSCL9uZh5ZcXDcPzQ_-kU7P7Q1",  // IMG-20260401-WA0009.jpg
        "13P--boXVqZQxLbZ3M66RBDyV6mnAUOhb"   // IMG-20260401-WA0010.jpg
    ];
    
    function getImagenURL(id) {
        if (id) {
            return `https://drive.google.com/uc?export=view&id=${id}`;
        }
        return null;
    }
    
    // =======================================================
    // 2. PRODUCTOS (100 unidades)
    // =======================================================
    const PRECIO_UNITARIO = 22000;
    const TALLES = "S al XXL";
    
    const equiposBase = [
        "Platense", "Estudiantes", "Chicago", "Aldosivi", "River", "Boca", 
        "Racing", "Independiente", "San Lorenzo", "Newell's", "Rosario Central",
        "Real Madrid", "Barcelona", "PSG", "Milan", "Inter", "Juventus",
        "Manchester Utd", "Liverpool", "Arsenal", "Selección Argentina",
        "Selección Brasil", "Selección Uruguay"
    ];
    
    let productos = [];
    
    for (let i = 1; i <= 100; i++) {
        let equipo = equiposBase[(i-1) % equiposBase.length];
        let nombre = `Remera ${equipo}`;
        let imagenID = null;
        // Asigno las 7 imágenes a los primeros 7 productos (Platense, Estudiantes, Chicago, etc)
        if (i <= imagenesIDs.length) {
            imagenID = imagenesIDs[i-1];
        }
        productos.push({
            id: i,
            nombre: nombre,
            precio: PRECIO_UNITARIO,
            talles: TALLES,
            imagenID: imagenID
        });
    }
    
    // =======================================================
    // 3. CARRITO
    // =======================================================
    let carrito = [];
    
    function guardarCarrito() {
        localStorage.setItem('carrito_sincompetencia', JSON.stringify(carrito));
        actualizarContadorCarrito();
        renderCarritoModal();
    }
    
    function cargarCarrito() {
        const stored = localStorage.getItem('carrito_sincompetencia');
        if(stored) {
            carrito = JSON.parse(stored);
        } else {
            carrito = [];
        }
        actualizarContadorCarrito();
        renderCarritoModal();
    }
    
    function actualizarContadorCarrito() {
        const totalItems = carrito.reduce((acc, item) => acc + item.cantidad, 0);
        document.getElementById('cartCount').innerText = totalItems;
    }
    
    function agregarAlCarrito(idProducto) {
        const producto = productos.find(p => p.id === idProducto);
        if(!producto) return;
        const existente = carrito.find(item => item.id === idProducto);
        if(existente) {
            existente.cantidad++;
        } else {
            carrito.push({
                id: producto.id,
                nombre: producto.nombre,
                precio: producto.precio,
                cantidad: 1,
                talles: producto.talles,
                imagenID: producto.imagenID
            });
        }
        guardarCarrito();
    }
    
    function cambiarCantidad(id, delta) {
        const idx = carrito.findIndex(item => item.id === id);
        if(idx !== -1) {
            const nuevaCant = carrito[idx].cantidad + delta;
            if(nuevaCant <= 0) {
                carrito.splice(idx,1);
            } else {
                carrito[idx].cantidad = nuevaCant;
            }
            guardarCarrito();
        }
    }
    
    function renderCarritoModal() {
        const container = document.getElementById('cartItemsList');
        if(carrito.length === 0) {
            container.innerHTML = '<p style="text-align:center;">🛍️ Carrito vacío</p>';
            document.getElementById('cartTotal').innerText = `Total: $0`;
            return;
        }
        let html = '';
        let total = 0;
        carrito.forEach(item => {
            const subtotal = item.precio * item.cantidad;
            total += subtotal;
            html += `
                <div class="cart-item">
                    <div class="cart-item-info">
                        <div class="cart-item-name">${item.nombre}</div>
                        <div class="cart-item-price">$${item.precio.toLocaleString()}</div>
                        <div style="font-size:0.7rem;">${item.talles}</div>
                    </div>
                    <div class="cart-item-qty">
                        <button onclick="cambiarCantidad(${item.id}, -1)">-</button>
                        <span>${item.cantidad}</span>
                        <button onclick="cambiarCantidad(${item.id}, 1)">+</button>
                    </div>
                </div>
            `;
        });
        container.innerHTML = html;
        document.getElementById('cartTotal').innerHTML = `Total: $${total.toLocaleString()}`;
    }
    
    // =======================================================
    // 4. PAGINACIÓN Y RENDER
    // =======================================================
    let paginaActual = 1;
    const PRODUCTOS_POR_PAGINA = 12;
    
    function mostrarProductos() {
        const inicio = (paginaActual - 1) * PRODUCTOS_POR_PAGINA;
        const fin = inicio + PRODUCTOS_POR_PAGINA;
        const productosPagina = productos.slice(inicio, fin);
        const grid = document.getElementById('productGrid');
        grid.innerHTML = '';
        
        productosPagina.forEach(prod => {
            const card = document.createElement('div');
            card.className = 'product-card';
            
            const imgUrl = getImagenURL(prod.imagenID);
            let imagenStyle = '';
            let imagenContent = '';
            
            if (imgUrl) {
                imagenStyle = `style="background-image: url('${imgUrl}');"`;
                imagenContent = '';
            } else {
                const colorFondo = `hsl(${prod.id * 37 % 360}, 70%, 55%)`;
                imagenStyle = `style="background-color: ${colorFondo}; background-image: none; display: flex; align-items: center; justify-content: center; font-weight:bold; font-size:1rem;"`;
                imagenContent = `🏈 ${prod.nombre}`;
            }
            
            card.innerHTML = `
                <div class="product-img" ${imagenStyle}>
                    ${imagenContent}
                </div>
                <div class="product-info">
                    <div class="product-name">${prod.nombre}</div>
                    <div class="product-sizes">Talles: ${prod.talles}</div>
                    <div class="product-price">$${prod.precio.toLocaleString()}</div>
                    <button class="add-to-cart" data-id="${prod.id}"><i class="fas fa-cart-plus"></i> Agregar</button>
                </div>
            `;
            grid.appendChild(card);
        });
        
        document.querySelectorAll('.add-to-cart').forEach(btn => {
            btn.addEventListener('click', (e) => {
                const id = parseInt(btn.getAttribute('data-id'));
                agregarAlCarrito(id);
            });
        });
        
        renderPaginacion();
    }
    
    function renderPaginacion() {
        const totalPaginas = Math.ceil(productos.length / PRODUCTOS_POR_PAGINA);
        const container = document.getElementById('paginationControls');
        container.innerHTML = '';
        for(let i = 1; i <= totalPaginas; i++) {
            const btn = document.createElement('button');
            btn.innerText = i;
            btn.classList.add('page-btn');
            if(i === paginaActual) btn.classList.add('active');
            btn.addEventListener('click', () => {
                paginaActual = i;
                mostrarProductos();
                window.scrollTo({ top: document.querySelector('.products-section').offsetTop - 70, behavior: 'smooth' });
            });
            container.appendChild(btn);
        }
    }
    
    // =======================================================
    // 5. MODAL Y CHECKOUT
    // =======================================================
    const modal = document.getElementById('cartModal');
    const overlay = document.getElementById('overlay');
    const cartIconBtn = document.getElementById('cartIcon');
    const closeCart = document.getElementById('closeCartBtn');
    
    function openCart() {
        modal.classList.add('open');
        overlay.classList.add('active');
        renderCarritoModal();
    }
    function closeCartModal() {
        modal.classList.remove('open');
        overlay.classList.remove('active');
    }
    cartIconBtn.addEventListener('click', openCart);
    closeCart.addEventListener('click', closeCartModal);
    overlay.addEventListener('click', closeCartModal);
    
    document.getElementById('checkoutBtn').addEventListener('click', () => {
        if(carrito.length === 0) {
            alert("Agregá productos al carrito antes de finalizar.");
            return;
        }
        let mensaje = "🛒 *COMPRA EN SINCOMPETENCIA*%0A";
        let totalFinal = 0;
        carrito.forEach(item => {
            const subtotal = item.precio * item.cantidad;
            totalFinal += subtotal;
            mensaje += `- ${item.nombre} x${item.cantidad} = $${subtotal.toLocaleString()}%0A`;
        });
        mensaje += `%0A*TOTAL: $${totalFinal.toLocaleString()}*%0A`;
        mensaje += `%0A📍 Envíos a todo el país. Local en Rosario.%0A`;
        mensaje += `¡Hola! Quiero realizar esta compra. Gracias.`;
        const url = `https://wa.me/5491159669909?text=${mensaje}`;
        window.open(url, '_blank');
    });
    
    // Inicializar
    cargarCarrito();
    mostrarProductos();
</script>
</body>
</html>
