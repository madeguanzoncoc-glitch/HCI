* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: 'Segoe UI', Arial, sans-serif;
  line-height: 1.6;
  color: #333;
  background-color: #f8fff8;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

/* Header */
header {
  background-color: rgba(255, 255, 255, 0.95);
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  padding: 15px 0;
  position: sticky;
  top: 0;
  z-index: 100;
}

header .container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 20px;
}

.logo-container {
  display: flex;
  align-items: center;
  gap: 12px;
}

.logo-img {
  height: 55px;
  width: auto;
}

.logo-text {
  color: #006400;
  font-size: 1.85rem;
  font-weight: 700;
}

.nav {
  display: flex;
  gap: 25px;
}

nav a {
  margin-left: 25px;
  text-decoration: none;
  color: #006400;
  font-weight: 500;
}

nav a:hover {
  color: #32CD32;
}

/* Candidates */
.candidate {
  min-height: 85vh;
  background-color: #006400;
  position: relative;
  display: flex;
  align-items: center;
  overflow: hidden;
}

.image {
  position: absolute;
  top: -3rem;
  left: 0;
  width: 50%;
  height: 120%;
  background-image: url('images/Coc.png');
  background-size: cover;
  background-repeat: no-repeat;
  z-index: 1;
}

.image::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0,100,0,0.65);
  z-index: 2;
}

.candidate-content {
  position: relative;
  z-index: 3;
  display: flex;
  gap: 80px;
  align-items: center;
  flex-wrap: wrap;
  width: 100%;
}

.candidate-text {
  flex: 1;
  min-width: 320px;
}

.candidate-text h1 {
  font-size: 3.8rem;
  font-weight: 700;
  color: white;
  line-height: 1.1;
  margin-bottom: 15px;
}

/* Slider */
.slider {
  flex: 1;
  min-width: 340px;
  max-width: 480px;
  height: 460px;
  position: relative;
  border-radius: 20px;
  overflow: hidden;
  box-shadow: 0 15px 40px rgba(0, 0, 0, 0.3);
}

.slide {
  position: absolute;
  inset: 0;
  opacity: 0;
  transition: opacity 0.8s;
  display: none;
}

.slide.active {
  opacity: 1;
  display: block;
}

.slide img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.slide-info {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  background: linear-gradient(transparent, rgba(0,0,0,0.85));
  color: white;
  padding: 40px 30px 30px;
}

.dots {
  position: absolute;
  bottom: 20px;
  left: 50%;
  transform: translateX(-50%);
  display: flex;
  gap: 10px;
}

.dot {
  width: 14px;
  height: 14px;
  background: rgba(255,255,255,0.6);
  border-radius: 50%;
  cursor: pointer;
}

.dot.active {
  background: #32CD32;
  transform: scale(1.2);
}

/* Common */
.candidates, .about, .rules, .contact {
  padding: 100px 0;
  background-color: #f8fff8;
}

.section-title {
 text-align: center;
 font-size: 3.2rem;
 font-weight: 700;
 color: #006400;
 margin: 0 auto 70px auto;
 position: relative;
 display: block;
 padding-bottom: 20px;
 letter-spacing: -0.015rem;
 text-shadow: 0 2px 6px rgba(0,100,0,0.12);
}

.section-title::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 50%;
  transform: translateX(-50%);
  width: 120px;
  height: 5px;
  background: linear-gradient(to right, #32CD32, #006400);
  border-radius: 3px;
}

/* Candidates */
.candidates-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 30PX;
}

.candidate-card {
  background:  white;
  border-radius: 16px;
  overflow: hidden;
  box-shadow: 0 8px 25px rgba(0, 100, 0, 0.12);
  text-align: center;
  transition: all 0.3s ease;
  height: 100%;
}

.candidate-card:hover {
  transform: translateY(-12px);
  box-shadow: 0 15px 35px rgba(0,100,0,0.2);
}

.candidate-image {
  height: 260px;
  overflow: hidden;
}

.candidate-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.candidate-card h3 {
  margin: 18px 0 6px;
  color: #006400;
}

.position-title {
  text-align: center;
  font-size: 1.8rem;
  color: #006400;
  margin: 50px 0 30px;
  font-weight: 600;
  display: inline-block;
  padding: 10px 24px;
  background-color: #006400;
  color: white;
  text-decoration: none;
  border-radius: 50px;
  transition: all 0.3s ease;
  white-space: nowrap;
}

.position {
  color: #555;
  margin-bottom: 18px;
  font-size: 1rem;
}

.button {
  display: inline-block;
  padding: 10px 24px;
  background-color: #006400;
  color: white;
  text-decoration: none;
  font-weight: 600;
  border-radius: 50px;
  margin-left: 40px;
  transition: all 0.3s ease;
  white-space: nowrap;

}

.button:hover {
  background-color: #004d00;
  transform: translateY(-2px);
}

.vote-btn {
  background-color: #32CD32;
  color: white;
  border: none;
  padding: 14px 40px;
  font-size: 1.1rem;
  font-weight: 600;
  border-radius: 50px;
  cursor: pointer;
  margin-bottom: 25px;
}

.vote-btn:hover {
  background-color: #006400;
}

/* About */
.about-grid {
  display: flex;
  gap: 60px;
  align-items: center;
  flex-wrap: wrap;
}

.about-video {
  flex: 1;
  min-width: 400px;
  position: relative;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
}

.about-video video {
  width: 100%;
  height: auto;
  display: block;
}

.about-overlay {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  background: rgba(0, 0, 0, 0.75);
  color: white;
  padding: 25px;
  text-align: center;
}

.about-overlay h3 {
  font-size: 1.6rem;
  margin-bottom: 8px;
}

.about-text {
  flex: 1;
  min-width: 400px;
}

.about-text h2 {
  font-size: 2.9rem;
  font-weight: 700;
  color: #006400;
  margin-bottom: 28px;
  line-height: 1.1;
}

.about-text p {
  font-size: 1.18rem;
  line-height: 1.75;
  color: #444;
  margin-bottom: 22px;
}

.about-text p:last-of-type {
  margin-bottom: 35px;
}

.learn-more-btn {
  background-color: #006400;
  color: white;
  padding: 14px 36px;
  border-radius: 50px;
  text-decoration: none;
  font-weight: 600;
  font-size: 1.05rem;
  display: inline-block;
  transition: all 0.3s ease;
}

.learn-more-btn:hover {
  background-color: #004d00;
  transform: translateY(-2px);
}


/* Contact Us */
.contact {
  background-color: #006400;
  color: white;
  padding: 100px 0;
}

.contact .section-title {
  color: white;
}

.contact-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 40px;
}

.contact-card {
  background: rgba(255,255,255,0.1);
  padding: 30px;
  border-radius: 12px;
}

.contact-card h3 {
  color: #90EE90;
  margin-bottom: 20px;
  font-size: 1.5rem;
}

.info-row {
  display: flex;
  align-items: flex-start;
  gap: 12px;
  margin-bottom: 14px;
  font-size: 1.05rem;
}

.info-row .icon {
  font-size: 1.3rem;
  min-width: 24px;
}

/* Footer */
footer {
  background-color: #004d00;
  color: white;
  padding: 40px 0;
  text-align: center;
}

.green-separator {
  height: 4px;
  background: linear-gradient(to right, #32CD32);
  margin: 40px 0;
}

.rule-grid {
  max-width: 1000px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 25px;
}

.rules-box {
  background: white;
  padding: 32px 28px;
  border-radius: 16px;
  box-shadow: 0 8px 25px rgba(0,100,0,0.1);
  border-left: 6px solid #32CD32;
  transition: all 0.3s ease;
  position: relative;
}

.rules-box:hover {
  transform: translateY(-8px);
  box-shadow: 0 15px 35px rgba(0,100,0,0.18);
}

.rule-number {
  position: absolute;
  top: 20px;
  right: 25px;
  font-size: 2.2rem;
  font-weight: 700;
  color: rgba(50,205,50,0.15);
  line-height: 1;
}

.rules-box h3 {
  color: #006400;
  font-size: 1.4rem;
  margin-bottom: 14px;
  font-weight: 600;
  padding-right: 50px;
}

.rules-box p {
  color: #444;
  line-height: 1.7;
  font-size: 1.05rem;
}

.main-title {
  font-size: 4.5rem;
  font-weight: 800;
  color: white;
  line-height: 1.05;
  margin-bottom: 25px;
  text-shadow: 0 6px 15px rgba(0,0,0,0.45);
  letter-spacing: -0.04rem;
}

.candidate-text .tagline {
  font-size: 1.75rem;
  color: #a0ff9e;
  font-weight: 700;
  margin-bottom: 20px;
  text-shadow: 0 3px 10px rgba(0,0,0,0.4);
}

.candidate-text .description {
  font-size: 1.4rem;
  color: rgba(255,255,255,0.97);
  max-width: 520px;
  line-height: 1.6;
  text-shadow: 0 2px 8px rgba(0,0,0,0.35);
}
