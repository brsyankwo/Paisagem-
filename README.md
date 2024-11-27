# Paisagem-
/* Estilos gerais */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  overflow: hidden;
  font-family: Arial, sans-serif;
}
.sky {
  background: linear-gradient(to bottom, #87CEEB, #F0E68C);
  height: 100vh;
  width: 100vw;
  position: relative;
  overflow: hidden;
}

/* Sol */
.sun {
  width: 100px;
  height: 100px;
  background: radial-gradient(circle, #FFD700, #FFA500);
  border-radius: 50%;
  position: absolute;
  top: 80%;
  left: 50%;
  transform: translateX(-50%);
  box-shadow: 0 0 50px #FFD700;
  animation: sunrise 10s infinite alternate ease-in-out;
}

/* Animação do sol */
@keyframes sunrise {
  0% {
    top: 80%;
  }
  50% {
    top: 10%;
  }
  100% {
    top: 80%;
  }
}

/* Nuvens */
.cloud {
  width: 150px;
  height: 50px;
  background: #fff;
  border-radius: 50%;
  position: absolute;
  opacity: 0.8;
  animation: moveClouds 15s infinite linear;
}
.cloud::before,
.cloud::after {
  content: '';
  position: absolute;
  background: #fff;
  border-radius: 50%;
}
.cloud::before {
  width: 100px;
  height: 50px;
  top: -20px;
  left: 20px;
}
.cloud::after {
  width: 120px;
  height: 60px;
  top: 10px;
  left: -20px;
}
.cloud1 {
  top: 20%;
  left: -10%;
  animation-delay: 0s;
}
.cloud2 {
  top: 40%;
  left: -20%;
  animation-delay: 5s;
}
.cloud3 {
  top: 60%;
  left: -30%;
  animation-delay: 10s;
}
@keyframes moveClouds {
  0% {
    left: -30%;
  }
  100% {
    left: 130%;
  }
}

/* Montanhas */
.mountains {
  position: absolute;
  bottom: 30%;
  width: 100%;
  height: 40%;
  background: linear-gradient(to top, #2E8B57, #3CB371);
  clip-path: polygon(0 100%, 15% 60%, 30% 100%, 50% 50%, 70% 100%, 85% 60%, 100% 100%);
}

/* Grama */
.grass {
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 30%;
  background: linear-gradient(to top, #228B22, #32CD32);
}

/* Lago */
.lake {
  position: absolute;
  bottom: 10%;
  left: 20%;
  width: 60%;
  height: 20%;
  background: linear-gradient(to top, #4682B4, #5F9EA0);
  border-radius: 50%;
  opacity: 0.8;
  animation: ripple 4s infinite;
}

/* Animação do lago */
@keyframes ripple {
  0% {
    transform: scale(1);
    opacity: 0.8;
  }
  50% {
    transform: scale(1.05);
    opacity: 0.6;
  }
  100% {
    transform: scale(1);
    opacity: 0.8;
  }
}
