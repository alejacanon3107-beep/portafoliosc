<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi Portafolio Profesional</title>
    <style>
        :root {
            --primary: #2563eb;
            --bg: #0f172a;
            --card-bg: #1e293b;
            --text: #f8fafc;
            --text-muted: #94a3b8;
        }
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
        }
        body {
            background-color: var(--bg);
            color: var(--text);
            line-height: 1.6;
        }
        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1.5rem 5%;
            background: rgba(15, 23, 42, 0.9);
            position: sticky;
            top: 0;
            border-bottom: 1px solid #334155;
            z-index: 100;
        }
        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            color: var(--primary);
        }
        nav ul {
            display: flex;
            list-style: none;
            gap: 1.5rem;
        }
        nav a {
            color: var(--text-muted);
            text-decoration: none;
            transition: color 0.3s;
        }
        nav a:hover {
            color: var(--primary);
        }
        .hero {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 6rem 1rem;
            max-width: 800px;
            margin: 0 auto;
        }
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
        }
        .hero h1 span {
            color: var(--primary);
        }
        .hero p {
            font-size: 1.2rem;
            color: var(--text-muted);
            margin-bottom: 2rem;
        }
        .btn {
            background-color: var(--primary);
            color: white;
            padding: 0.75rem 1.5rem;
            border-radius: 0.375rem;
            text-decoration: none;
            font-weight: 600;
            transition: opacity 0.3s;
        }
        .btn:hover {
            opacity: 0.9;
        }
        section {
            padding: 4rem 10%;
            max-width: 1200px;
            margin: 0 auto;
        }
        section h2 {
            font-size: 2rem;
            margin-bottom: 2rem;
            border-bottom: 2px solid var(--primary);
            display: inline-block;
            padding-bottom: 0.5rem;
        }
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }
        .card {
            background-color: var(--card-bg);
            padding: 1.5rem;
            border-radius: 0.5rem;
            border: 1px solid #334155;
        }
        .card h3 {
            margin-bottom: 0.75rem;
        }
        .card p {
            color: var(--text-muted);
            font-size: 0.95rem;
        }
        footer {
            text-align: center;
            padding: 2rem;
            background-color: #090d16;
            color: var(--text-muted);
            border-top: 1px solid #334155;
            margin-top: 4rem;
        }
    </style>
</head>
<body>

    <header>
        <div class="logo">MiPortafolio</div>
        <nav>
            <ul>
                <li><a href="#sobre-mi">Sobre mí</a></li>
                <li><a href="#proyectos">Proyectos</a></li>
                <li><a href="#contacto">Contacto</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <!-- SECCIÓN PRINCIPAL / INICIO -->
        <div class="hero">
            <h1>Hola, soy <span>Tu Nombre</span></h1>
            <p>Desarrollador web y creador digital especializado en construir experiencias interactivas y funcionales.</p>
            <a href="#proyectos" class="btn">Ver Proyectos</a>
        </div>

        <!-- SECCIÓN SOBRE MÍ -->
        <section id="sobre-mi">
            <h2>Sobre mí</h2>
            <p>Tengo experiencia diseñando y estructurando páginas web eficientes. Me apasiona transformar ideas complejas en interfaces limpias, adaptables a cualquier dispositivo y fáciles de usar.</p>
        </section>

        <!-- SECCIÓN DE PROYECTOS -->
        <section id="proyectos">
            <h2>Mis Proyectos</h2>
            <div class="grid">
                <div class="card">
                    <h3>Proyecto 1</h3>
                    <p>Descripción breve sobre qué tecnología utilizaste en este proyecto y qué problema resuelve.</p>
                </div>
                <div class="card">
                    <h3>Proyecto 2</h3>
                    <p>Descripción breve sobre este segundo trabajo o desarrollo realizado para tu portafolio.</p>
                </div>
                <div class="card">
                    <h3>Proyecto 3</h3>
                    <p>Descripción breve sobre otra aplicación o diseño web incluido en tu experiencia.</p>
                </div>
            </div>
        </section>

        <!-- SECCIÓN DE CONTACTO -->
        <section id="contacto">
            <h2>Contacto</h2>
            <p>¿Quieres ponerte en contacto conmigo o colaborar en un proyecto? Escríbeme a <strong>tucorreo@email.com</strong> o encuéntrame en mis redes profesionales.</p>
        </section>
    </main>

    <!-- PIE DE PÁGINA -->
    <footer>
        <p>&copy; 2026 Tu Nombre. Todos los derechos reservados.</p>
    </footer>

</body>
</html>
