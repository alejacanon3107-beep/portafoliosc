<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sara Cañón | Social Media Strategist</title>
    <style>
        :root {
            --primary: #e6007e;
            --primary-hover: #c4006b;
            --bg: #faf7f2;
            --card-bg: #ffffff;
            --text-dark: #1a1a1a;
            --text-muted: #666666;
            --border: #eeeeee;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', -apple-system, BlinkMacSystemFont, Roboto, sans-serif;
        }

        body {
            background-color: var(--bg);
            color: var(--text-dark);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* NAVEGACIÓN Y MENÚ MÓVIL */
        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 5%;
            background: rgba(250, 247, 242, 0.95);
            backdrop-filter: blur(8px);
            position: sticky;
            top: 0;
            z-index: 1000;
            border-bottom: 1px solid rgba(0, 0, 0, 0.05);
        }

        .logo {
            font-weight: 800;
            font-size: 1.2rem;
            letter-spacing: -0.5px;
            color: var(--text-dark);
        }

        /* Menú Hamburguesa para Celular */
        .menu-toggle {
            display: none;
            flex-direction: column;
            gap: 5px;
            cursor: pointer;
            background: none;
            border: none;
            padding: 5px;
        }

        .menu-toggle span {
            width: 25px;
            height: 3px;
            background-color: var(--text-dark);
            border-radius: 2px;
            transition: all 0.3s ease;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 1.5rem;
        }

        nav a {
            color: var(--text-dark);
            text-decoration: none;
            font-weight: 500;
            font-size: 0.95rem;
            transition: color 0.2s;
        }

        nav a:hover {
            color: var(--primary);
        }

        /* HERO / SECCIÓN PRINCIPAL */
        .hero {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            padding: 2.5rem 1rem 4rem 1rem;
            max-width: 900px;
            margin: 0 auto;
        }

        .poster-wrapper {
            width: 100%;
            max-width: 420px;
            margin-bottom: 2rem;
            border-radius: 16px;
            overflow: hidden;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.08);
            background: #fff;
        }

        .poster-wrapper img {
            width: 100%;
            height: auto;
            display: block;
            object-fit: contain;
        }

        .btn-main {
            display: inline-block;
            background-color: #1a1a1a;
            color: #ffffff;
            padding: 0.9rem 2.2rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            font-size: 1rem;
            transition: transform 0.2s, background-color 0.2s;
        }

        .btn-main:active {
            transform: scale(0.97);
        }

        /* SECCIONES Y CONTENIDO */
        section {
            padding: 3.5rem 6%;
            max-width: 1000px;
            margin: 0 auto;
        }

        section h2 {
            font-size: 1.8rem;
            margin-bottom: 1.5rem;
            text-align: center;
            color: var(--text-dark);
        }

        .profile-section {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 1.5rem;
            background: #ffffff;
            padding: 2rem;
            border-radius: 20px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.03);
            margin-bottom: 3rem;
        }

        .lego-avatar {
            width: 140px;
            height: 140px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid var(--primary);
            box-shadow: 0 8px 20px rgba(230, 0, 126, 0.2);
        }

        .profile-bio {
            text-align: center;
        }

        .profile-bio h3 {
            font-size: 1.4rem;
            color: var(--primary);
            margin-bottom: 0.5rem;
        }

        .grid-projects {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 1.5rem;
        }

        .card {
            background: #ffffff;
            border-radius: 16px;
            padding: 1.5rem;
            border: 1px solid var(--border);
            box-shadow: 0 4px 12px rgba(0,0,0,0.03);
        }

        .card h3 {
            font-size: 1.2rem;
            margin-bottom: 0.5rem;
            color: var(--text-dark);
        }

        .card p {
            color: var(--text-muted);
            font-size: 0.95rem;
        }

        footer {
            text-align: center;
            padding: 2rem 1rem;
            font-size: 0.9rem;
            color: var(--text-muted);
            border-top: 1px solid var(--border);
        }

        /* ADAPTACIÓN MÓVIL (MEDIA QUERIES) */
        @media (max-width: 768px) {
            .menu-toggle {
                display: flex;
            }

            nav {
                position: absolute;
                top: 100%;
                left: 0;
                width: 100%;
                background: #faf7f2;
                border-bottom: 1px solid var(--border);
                display: none;
                padding: 1rem 0;
                box-shadow: 0 10px 20px rgba(0,0,0,0.05);
            }

            nav.active {
                display: block;
            }

            nav ul {
                flex-direction: column;
                align-items: center;
                gap: 1.2rem;
            }

            .hero {
                padding-top: 1.5rem;
            }

            .poster-wrapper {
                max-width: 90%;
            }
        }
    </style>
</head>
<body>

    <header>
        <div class="logo">SARA CAÑÓN</div>
        <button class="menu-toggle" id="mobile-menu" aria-label="Abrir menú">
            <span></span>
            <span></span>
            <span></span>
        </button>
        <nav id="nav-menu">
            <ul>
                <li><a href="#sobre-mi">Sobre mí</a></li>
                <li><a href="#estrategia">Estrategia</a></li>
                <li><a href="#proyectos">Resultados</a></li>
                <li><a href="#contacto">Contacto</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <!-- AFICHE PRINCIPAL -->
        <div class="hero">
            <div class="poster-wrapper">
                <!-- Reemplaza la ruta si tu afiche tiene otro nombre -->
                <img src="poster.jpg" alt="Sara Cañón - Social Media Strategist">
            </div>
            <a href="#proyectos" class="btn-main">Ver proyectos</a>
        </div>

        <!-- FOTO DE LEGO Y PERFIL -->
        <section id="sobre-mi">
            <h2>Sobre mí</h2>
            <div class="profile-section">
                <!-- ASEGÚRATE DE GUARDAR TU FOTO DE LEGO COMO 'lego.jpg' EN LA MISMA CARPETA -->
                <img src="lego.jpg" alt="Foto de Lego Sara" class="lego-avatar">
                <div class="profile-bio">
                    <h3>Social Media Strategist & Influencer Marketing Jr</h3>
                    <p>Apasionada por la creación de contenido, estrategias digitales dinámicas y campañas con alto impacto visual y de interacción.</p>
                </div>
            </div>
        </section>

        <!-- SECCIÓN DE PROYECTOS -->
        <section id="proyectos">
            <h2>Estrategias y Proyectos</h2>
            <div class="grid-projects">
                <div class="card">
                    <h3>Investigación de Audiencias</h3>
                    <p>Análisis profundo de métricas y comportamientos para la optimización de contenido en redes.</p>
                </div>
                <div class="card">
                    <h3>Influencer Marketing</h3>
                    <p>Gestión y coordinación de campañas con creadores de contenido para ampliar el alcance de marca.</p>
                </div>
                <div class="card">
                    <h3>Creación de Contenido</h3>
                    <p>Diseño y ejecución de parrillas visuales dinámicas orientadas a la conversión y *engagement*.</p>
                </div>
            </div>
        </section>

        <!-- CONTACTO -->
        <section id="contacto">
            <h2>Contacto</h2>
            <p style="text-align: center;">¿Hablamos de tu próxima campaña?</p>
            <p style="text-align: center; font-weight: bold; margin-top: 0.5rem; color: var(--primary);">
                contacto@saracanon.com
            </p>
        </section>
    </main>

    <footer>
        <p>&copy; 2026 Sara Cañón. Todos los derechos reservados.</p>
    </footer>

    <!-- SCRIPT PARA EL MENÚ EN CELULAR -->
    <script>
        const menuToggle = document.getElementById('mobile-menu');
        const navMenu = document.getElementById('nav-menu');

        menuToggle.addEventListener('click', () => {
            navMenu.classList.toggle('active');
        });

        // Cerrar el menú al hacer clic en un enlace
        document.querySelectorAll('nav a').forEach(link => {
            link.addEventListener('click', () => {
                navMenu.classList.remove('active');
            });
        });
    </script>
</body>
</html>
