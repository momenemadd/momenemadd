<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jadoo Travel Agency</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&family=Volkhov:wght@700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #181E4B;
            --accent: #DF6951;
            --yellow: #F1A501;
            --text: #5E6282;
            --bg: #FFF;
            --gray: #E5E5E5;
        }
        * { box-sizing: border-box; margin: 0; padding: 0; }
        body {
            font-family: 'Poppins', Arial, sans-serif;
            background: var(--bg);
            color: var(--text);
        }
        header, nav, section, footer {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
        }
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 2rem 1rem 1rem 1rem;
        }
        .logo {
            font-family: 'Volkhov', serif;
            font-size: 2rem;
            color: var(--primary);
            font-weight: 700;
        }
        .nav-links {
            display: flex;
            gap: 2rem;
        }
        .nav-links a {
            text-decoration: none;
            color: #212832;
            font-weight: 500;
            font-size: 1rem;
        }
        .nav-actions {
            display: flex;
            gap: 1rem;
            align-items: center;
        }
        .btn-signup {
            border: 1px solid #212832;
            border-radius: 5px;
            padding: 0.5rem 1.5rem;
            background: none;
            color: #212832;
            font-weight: 500;
            cursor: pointer;
        }
        .lang {
            font-weight: 500;
            color: #212832;
            margin-left: 1rem;
        }
        .hero {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
            padding: 2rem 1rem 4rem 1rem;
            gap: 2rem;
        }
        .hero-content {
            flex: 1 1 350px;
            max-width: 500px;
        }
        .tagline {
            color: var(--accent);
            font-weight: 700;
            text-transform: uppercase;
            font-size: 1.1rem;
            margin-bottom: 1rem;
        }
        .hero-title {
            font-family: 'Volkhov', serif;
            font-size: 3rem;
            color: var(--primary);
            margin-bottom: 1rem;
            line-height: 1.1;
        }
        .hero-desc {
            font-size: 1.1rem;
            margin-bottom: 2rem;
        }
        .hero-cta {
            display: flex;
            gap: 1.5rem;
            align-items: center;
        }
        .btn-primary {
            background: var(--yellow);
            color: #fff;
            border: none;
            border-radius: 10px;
            padding: 1rem 2rem;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            box-shadow: 0 4px 16px rgba(241, 165, 1, 0.15);
        }
        .play-demo {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            color: #686D77;
            font-size: 1rem;
            cursor: pointer;
        }
        .play-circle {
            width: 2.5rem;
            height: 2.5rem;
            background: var(--accent);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #fff;
            font-size: 1.2rem;
        }
        .hero-img {
            flex: 1 1 350px;
            display: flex;
            justify-content: center;
        }
        .hero-img img {
            max-width: 350px;
            width: 100%;
            border-radius: 2rem;
        }
        .section-title {
            font-family: 'Volkhov', serif;
            font-size: 2.2rem;
            color: var(--primary);
            text-align: center;
            margin-bottom: 2rem;
        }
        .section-subtitle {
            text-align: center;
            color: var(--text);
            font-weight: 600;
            margin-bottom: 0.5rem;
            text-transform: uppercase;
        }
        .services {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 2rem;
            margin-bottom: 4rem;
        }
        .service-card {
            background: #fff;
            border-radius: 2rem;
            box-shadow: 0 4px 24px rgba(0,0,0,0.06);
            padding: 2rem 1.5rem;
            max-width: 250px;
            text-align: center;
            flex: 1 1 200px;
        }
        .service-icon {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }
        .service-title {
            font-weight: 600;
            color: #1E1D4C;
            margin-bottom: 0.5rem;
        }
        .destinations {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            justify-content: center;
            margin-bottom: 4rem;
        }
        .destination-card {
            background: #fff;
            border-radius: 1.5rem;
            box-shadow: 0 4px 24px rgba(0,0,0,0.06);
            max-width: 300px;
            flex: 1 1 250px;
            overflow: hidden;
        }
        .destination-img {
            width: 100%;
            height: 180px;
            object-fit: cover;
        }
        .destination-content {
            padding: 1rem;
        }
        .destination-title {
            font-weight: 600;
            color: var(--primary);
            margin-bottom: 0.5rem;
        }
        .destination-meta {
            display: flex;
            justify-content: space-between;
            color: var(--text);
            font-size: 0.95rem;
        }
        .steps {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            justify-content: center;
            margin-bottom: 4rem;
        }
        .step-card {
            background: #fff;
            border-radius: 1.5rem;
            box-shadow: 0 4px 24px rgba(0,0,0,0.06);
            padding: 1.5rem;
            max-width: 300px;
            flex: 1 1 200px;
            text-align: center;
        }
        .step-icon {
            font-size: 2rem;
            margin-bottom: 1rem;
        }
        .testimonials {
            background: #f9f9f9;
            padding: 3rem 1rem;
            border-radius: 2rem;
            margin-bottom: 4rem;
        }
        .testimonial-title {
            font-family: 'Volkhov', serif;
            font-size: 2rem;
            color: var(--primary);
            text-align: center;
            margin-bottom: 2rem;
        }
        .testimonial-list {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            justify-content: center;
        }
        .testimonial-card {
            background: #fff;
            border-radius: 1.5rem;
            box-shadow: 0 4px 24px rgba(0,0,0,0.06);
            padding: 2rem;
            max-width: 350px;
            
            flex: 1 1 250px;
        }
        .testimonial-user {
            font-weight: 600;
            color: var(--primary);
            margin-top: 1rem;
        }
        .partners {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            justify-content: center;
            align-items: center;
            margin-bottom: 4rem;
        }
        .partner-logo {
            width: 200px;
            height: 40px;
            background: #eee;
            border-radius: 0.5rem;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
            color: #888;
        }
        .newsletter {
            background: #f3f0fa;
            border-radius: 2rem;
            padding: 2rem 1rem;
            text-align: center;
            margin-bottom: 4rem;
        }
        .newsletter-title {
            font-size: 1.5rem;
            font-weight: 600;
            color: var(--text);
            margin-bottom: 1rem;
        }
        .newsletter-form {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-top: 1rem;
        }
        .newsletter-input {
            padding: 0.75rem 1rem;
            border-radius: 0.5rem;
            border: 1px solid #ccc;
            font-size: 1rem;
            width: 250px;
        }
        .newsletter-btn {
            background: linear-gradient(180deg, #FF946D 0%, #FF7D68 100%);
            color: #fff;
            border: none;
            border-radius: 0.5rem;
            padding: 0.75rem 2rem;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
        }
        footer {
            background: #fff;
            padding: 2rem 1rem 1rem 1rem;
            border-top: 1px solid #eee;
            text-align: center;
        }
        .footer-cols {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            justify-content: center;
            margin-bottom: 2rem;
        }
        .footer-col {
            min-width: 120px;
        }
        .footer-title {
            font-weight: 700;
            color: var(--primary);
            margin-bottom: 0.5rem;
        }
        .footer-link {
            color: var(--text);
            text-decoration: none;
            display: block;
            margin-bottom: 0.25rem;
            font-size: 1rem;
        }
        .footer-logo {
            font-family: 'Volkhov', serif;
            font-size: 2rem;
            color: var(--primary);
            font-weight: 700;
            margin-bottom: 0.5rem;
        }
        .footer-desc {
            color: var(--text);
            font-size: 0.95rem;
            margin-bottom: 1rem;
        }
        .footer-social {
            display: flex;
            gap: 1rem;
            justify-content: center;
            margin-bottom: 1rem;
        }
        .footer-social a {
            width: 2.2rem;
            height: 2.2rem;
            background: #fff;
            border-radius: 50%;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            color: #080809;
            font-size: 1.2rem;
            text-decoration: none;
        }
        @media (max-width: 900px) {
            .hero, .services, .destinations, .steps, .testimonial-list, .partners, .footer-cols {
                flex-direction: column;
                align-items: center;
            }
            nav, header, section, footer {
                max-width: 100%;
            }
        }
        @media (max-width: 600px) {
            .hero-title { font-size: 2rem; }
            .section-title { font-size: 1.3rem; }
            .testimonial-title { font-size: 1.2rem; }
        }
    </style>
</head>
<body>
    <nav>
        <div class="logo">Jadoo</div>
        <div class="nav-links">
            <a href="#destinations">Destinations</a>
            <a href="#hotels">Hotels</a>
            <a href="#flights">Flights</a>
            <a href="#bookings">Bookings</a>
            <a href="#login">Login</a>
        </div>
        <div class="nav-actions">
            <button class="btn-signup">Sign up</button>
            <span class="lang">EN</span>
        </div>
    </nav>
    <header class="hero">
        <div class="hero-content">
            <div class="tagline">Best Destinations around the world</div>
            <div class="hero-title">Travel, enjoy<br>and live a new<br>and full life</div>
            <div class="hero-desc">Built Wicket longer admire do barton vanity itself do in it. Preferred to sportsmen it engrossed listening. Park gate sell they west hard for the.</div>
            <div class="hero-cta">
                <button class="btn-primary">Find out more</button>
                <div class="play-demo">
                    <span class="play-circle">▶</span> Play Demo
                </div>
            </div>
        </div>
        <div class="hero-img">
            <img src="c:\Users\Momen\Desktop\jadoo\Traveller 1.png"  alt="Traveler" />
          
           
        </div>
    </header>
    <section>
        <div class="section-subtitle">Category</div>
        <div class="section-title">We Offer Best Services</div>
        <div class="services">
            <div class="service-card">
                <div class="service-icon"> <img src="c:\Users\Momen\Desktop\jadoo\satlite.png" alt="satlite" /></div>
                <div class="service-title">Calculated Weather</div>
                <div>Built Wicket longer admire do barton vanity itself do in it.</div>
            </div>
            <div class="service-card">
                <div class="service-icon"><img src="c:\Users\Momen\Desktop\jadoo\plane.png" alt="plane"></div>
                <div class="service-title">Best Flights</div>
                <div>Engrossed listening. Park gate sell they west hard for the.</div>
            </div>
            <div class="service-card">
                <div class="service-icon"><img src="c:\Users\Momen\Desktop\jadoo\mic.png" alt="mic"></div>
                <div class="service-title">Local Events</div>
                <div>Barton vanity itself do in it. Preferd to men it engrossed listening.</div>
            </div>
            <div class="service-card">
                <div class="service-icon"><img src="c:\Users\Momen\Desktop\jadoo\settings.png " alt="settings"></div>
                <div class="service-title">Customization</div>
                <div>We deliver outsourced aviation services for military customers</div>
            </div>
        </div>
    </section>
    <section id="destinations">
        <div class="section-subtitle">Top Selling</div>
        <div class="section-title">Top Destinations</div>
        <div class="destinations">
            <div class="destination-card">
                <img class="destination-img" src="https://images.unsplash.com/photo-1467269204594-9661b134dd2b?auto=format&fit=facearea&w=400&q=80" alt="Rome, Italy">
                <div class="destination-content">
                    <div class="destination-title">Rome, Italy</div>
                    <div class="destination-meta">
                        <span>$5,42k</span>
                        <span>10 Days Trip</span>
                    </div>
                </div>
            </div>
            <div class="destination-card">
                <img class="destination-img" src="https://images.unsplash.com/photo-1505761671935-60b3a7427bad?auto=format&fit=facearea&w=400&q=80" alt="London, UK">
                <div class="destination-content">
                    <div class="destination-title">London, UK</div>
                    <div class="destination-meta">
                        <span>$4.2k</span>
                        <span>12 Days Trip</span>
                    </div>
                </div>
            </div>
            <div class="destination-card">
                <img class="destination-img" src="https://images.unsplash.com/photo-1500534314209-a25ddb2bd429?auto=format&fit=facearea&w=400&q=80" alt="Full Europe">
                <div class="destination-content">
                    <div class="destination-title">Full Europe</div>
                    <div class="destination-meta">
                        <span>$15k</span>
                        <span>28 Days Trip</span>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <section>
        <div class="section-subtitle">Easy and Fast</div>
        <div class="section-title">Book Your Next Trip In 3 Easy Steps</div>
        <div class="steps">
            <div class="step-card">
                <div class="step-icon">📍</div>
                <div class="service-title">Choose Destination</div>
                <div>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Urna, tortor tempus.</div>
            </div>
            <div class="step-card">
                <div class="step-icon">💳</div>
                <div class="service-title">Make Payment</div>
                <div>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Urna, tortor tempus.</div>
            </div>
            <div class="step-card">
                <div class="step-icon">🛫</div>
                <div class="service-title">Reach Airport on Selected Date</div>
                <div>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Urna, tortor tempus.</div>
            </div>
        </div>
    </section>
    <section class="testimonials">
        <div class="testimonial-title">What People Say About Us.</div>
        <div class="testimonial-list">
           
            <div class="testimonial-card">
                <img class="icon-img" src="c:\Users\Momen\Desktop\jadoo\Image.png" alt="Image">
                <div>"On the Windows talking painted pasture yet its express parties use. Sure last upon he same as knew next. Of believed or diverted no."</div>
                <div class="testimonial-user">Chris Thomas</div>
                <div>CEO of Red Button</div>
            </div>
        </div>
    </section>
    <section>
        <div class="partners">
            <div class="partner-logo"><img class="img" src="c:\Users\Momen\Desktop\jadoo\axon.png" alt="axon"></div>
            <div class="partner-logo"><img class="img" src="c:\Users\Momen\Desktop\jadoo\jetstat.png" alt="jetstat"></div>
            <div class="partner-logo"><img class="img" src="c:\Users\Momen\Desktop\jadoo\expedia.png" alt="expedia"></div>
             <div class="partner-logo"><img class="img" src="c:\Users\Momen\Desktop\jadoo\qantas.png" alt="qantas"></div>
              <div class="partner-logo"><img class="img" src="c:\Users\Momen\Desktop\jadoo\alitalia.png" alt="alitalia"></div>
           
        </div>
    </section>
    <section class="newsletter">
        <div class="newsletter-title">Subscribe to get information, latest news and other interesting offers about Jadoo</div>
        <form class="newsletter-form">
            <input class="newsletter-input" type="email" placeholder="Your email" required />
            <button class="newsletter-btn" type="submit">Subscribe</button>
        </form>
    </section>
    <footer>
        <div class="footer-cols">
            <div class="footer-col">
                <div class="footer-logo">Jadoo.</div>
                <div class="footer-desc">Book your trip in minute, get full control for much longer.</div>
                <div class="footer-social">
                    <img class="footer-img" src="c:\Users\Momen\Desktop\jadoo\Social.png" alt="Social">
                   
                </div>
            </div>
            <div class="footer-col">
                <div class="footer-title">Company</div>
                <a class="footer-link" href="#">About</a>
                <a class="footer-link" href="#">Careers</a>
                <a class="footer-link" href="#">Mobile</a>
            </div>
            <div class="footer-col">
                <div class="footer-title">Contact</div>
                <a class="footer-link" href="#">Help/FAQ</a>
                <a class="footer-link" href="#">Press</a>
                <a class="footer-link" href="#">Affiliates</a>
            </div>
            <div class="footer-col">
                <div class="footer-title">More</div>
                <a class="footer-link" href="#">Airlinefees</a>
                <a class="footer-link" href="#">Airline</a>
                <a class="footer-link" href="#">Low fare tips</a>
            </div>
        </div>
        <div style="color: var(--text); font-size: 0.95rem;">All rights reserved@jadoo.co</div>
    </footer>
</body>
</html>
