<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Eventastic</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <nav>
            <div class="navbar-brand">
                <a href="/login">
                    <img src="images/auth.png" alt="Eventastic" style="height: 25px; width: auto;">
                </a>
                <a href="#">Eventastic</a>
            </div>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="/login">Log in</a></li>
                <li><a href="#contacts">Contact US</a></li>
            </ul>
            <a class="btn btn-primary" href="#pricing-cards">Plan's</a>
        </nav>
    </header>

    <section class="hero">
        <div class="hero-content">
            <h1>Unleash Fun</h1>
            <p>Online invitations card... Just got easier!</p>
            <a class="btn btn-white-outline" href="/dashboard">Dashboard</a>
        </div>
    </section>

    <section class="pricing" id="pricing-cards">
        <h2>Choose Wisely</h2>
        <div class="pricing-cards">
            <div class="card">
                <h3>Floral Template</h3>
                <p>Invitation card</p>
                <img src="images/Floral.png" alt="Floral Template">
                <ul>
                    <li>Online invitation card (General Link)</li>
                    <li>Customizable décor options to match your unique event theme.</li>
                </ul>
                <a href="https://wa.me/96171873634" class="btn btn-primary">Contact</a>
            </div>
            <div class="card">
                <h3>Mono Template</h3>
                <p>Invitation card</p>
                <img src="images/Mono.png" alt="Mono Template">
                <ul>
                    <li>Online invitation cards with individualized guest number</li>
                    <li>Customizable décor options to match your unique event theme.</li>
                </ul>
                <a href="https://wa.me/96171873634" class="btn btn-primary">Contact</a>
            </div>
            <div class="card">
                <h3>Galleria Template</h3>
                <p>Invitation card</p>
                <img src="images/back.PNG" alt="Galleria Template">
                <ul>
                    <li>Customizable décor options to match your unique event theme.</li>
                    <li>Page includes the ability to showcase up to 10 photos of your choice</li>
                </ul>
                <a href="https://wa.me/96171873634" class="btn btn-primary">Contact</a>
            </div>
        </div>
    </section>

    <section class="about" id="about-us">
        <h2>What do you need to create a wedding invitation e-card?</h2>
        <ul>
            <li>4 - 5 nice photos of the couple</li>
            <li>Bride's full name</li>
            <li>Groom's full name</li>
            <li>Wedding date</li>
            <li>Wedding ceremony location and time (optional)</li>
            <li>Wedding party location and time (optional)</li>
            <li>Email address</li>
            <li>Phone number</li>
        </ul>
    </section>

    <section class="gallery" id="gallery">
        <h2>Gallery</h2>
        <div class="gallery-images">
            <img src="images/photo-1601601392622-5d18104a78fe.jpeg" alt="Gallery Image">
            <img src="images/photo-1561185340-92902836cf7d.jpeg" alt="Gallery Image">
            <img src="images/photo-1628436710620-f505080824f5.jpeg" alt="Gallery Image">
            <img src="images/photo-1523580494863-6f3031224c94.jpeg" alt="Gallery Image">
        </div>
    </section>

    <section class="faq" id="faq">
        <h2>Curious Minds</h2>
        <div class="faq-item">
            <h3>How do I register for an event?</h3>
            <p>Simply click on the 'Register Now' button in the navbar on the event page and follow the easy steps to secure your spot!</p>
        </div>
        <div class="faq-item">
            <h3>Can I customize my event package?</h3>
            <p>Absolutely! We offer a range of customization options to tailor your event to your preferences and needs.</p>
        </div>
        <div class="faq-item">
            <h3>What types of events do you plan?</h3>
            <p>From extravagant galas to intimate gatherings, we specialize in creating unforgettable experiences for all occasions.</p>
        </div>
        <div class="faq-item">
            <h3>Do you provide event coordination services?</h3>
            <p>Yes, our expert team will handle every detail to ensure your event runs smoothly from start to finish.</p>
        </div>
    </section>

    <section class="contacts" id="contacts">
        <h2>Get in Touch</h2>
        <div class="contact-info">
            <div class="contact-item">
                <h3>Phone</h3>
                <p><a href="https://wa.me/96171873634">+961 70 26 11 81</a></p>
            </div>
            <div class="contact-item">
                <h3>Email</h3>
                <p><a href="mailto:moussaelie497@gmail.com">moussaelie497@gmail.com</a></p>
            </div>
            <div class="contact-item">
                <h3>Address</h3>
                <p>Beirut Lebanon</p>
            </div>
            <div class="contact-item">
                <h3>Opening Hours</h3>
                <p>Mon-Fri: 9am-6pm</p>
            </div>
        </div>
    </section>

    <footer>
        <p>© 2024 Let's Party All Night</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
 body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
    color: #333;
}

header {
    background-color: #333;
    color: #fff;
    padding: 10px 0;
    text-align: center;
}

nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 20px;
}

.navbar-brand a {
    color: #fff;
    text-decoration: none;
    font-size: 1.5rem;
}

nav ul {
    list-style: none;
    display: flex;
    gap: 20px;
}

nav ul li a {
    color: #fff;
    text-decoration: none;
}

.btn {
    padding: 10px 20px;
    background-color: #007BFF;
    color: #fff;
    border: none;
    cursor: pointer;
    text-decoration: none;
}

.btn-primary {
    background-color: #007BFF;
}

.btn-white-outline {
    background-color: transparent;
    border: 1px solid #fff;
}

.hero {
    background-image: url('images/back.PNG');
    background-size: cover;
    background-position: center;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    color: #fff;
}

.hero h1 {
    font-size: 3rem;
}

.hero p {
    font-size: 1.5rem;
}

.pricing {
    padding: 50px 20px;
    text-align: center;
}

.pricing-cards {
    display: flex;
    justify-content: center;
    gap: 20px;
    flex-wrap: wrap;
}

.card {
    background-color: #fff;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    padding: 20px;
    width: 300px;
    text-align: center;
}

.card img {
    width: 100%;
    border-radius: 8px;
}

.about, .gallery, .faq, .contacts {
    padding: 50px 20px;
    text-align: center;
}

.gallery-images {
    display: flex;
    justify-content: center;
    gap: 20px;
    flex-wrap: wrap;
}

.gallery-images img {
    width: 200px;
    border-radius: 8px;
}

.faq-item {
    margin-bottom: 20px;
}

.contact-info {
    display: flex;
    justify-content: center;
    gap: 20px;
    flex-wrap: wrap;
}

.contact-item {
    background-color: #fff;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    padding: 20px;
    width: 200px;
    text-align: center;
}

footer {
    background-color: #333;
    color: #fff;
    text-align: center;
    padding: 20px 0;
}
// Einfache JavaScript-Funktionen können hier hinzugefügt werden
document.addEventListener('DOMContentLoaded', function() {
    console.log('Website geladen');
});
