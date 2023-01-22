<template>
    <div class="wrap">
        <button class="button"><i class="fa-solid fa-phone"></i></button>
    </div>
</template>
<style lang="scss" scoped>
.wrap {
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.button {
  min-width: 60px;
  min-height: 60px;
  font-family: 'Nunito', sans-serif;
  font-size: 22px;
  text-transform: uppercase;
  letter-spacing: 1.3px;
  font-weight: 700;
  color: #c5c5c5;
background: linear-gradient(90deg, #808080 0%, #808080 100%);
  border: none;
  border-radius: 100px;
  box-shadow: 12px 12px 24px #808080;
  transition: all 0.3s ease-in-out 0s;
  cursor: pointer;
  outline: none;
  position: relative;
  padding: 10px;
  }

.button::before {
content: '';
  border-radius: 1000px;
  min-width: calc(60px + 12px);
  min-height: calc(60px + 12px);
  border: 6px solid #cfb53b;
  box-shadow: 0 0 60px #cfb53b;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  opacity: 0;
  transition: all .3s ease-in-out 0s;
}

.button:hover, .button:focus {
  color: #cfb53b;
  transform: translateY(-6px);
}

.button:hover::before, button:focus::before {
  opacity: 1;
}

.button::after {
  content: '';
  width: 10px; height: 10px;
  border-radius: 100%;
  border: 6px solid #808080;
  position: absolute;
  z-index: -1;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  animation: ring 1.5s infinite;
}

.button:hover::after, button:focus::after {
  animation: none;
  display: none;
}

@keyframes ring {
  0% {
    width: 30px;
    height: 30px;
    opacity: 1;
  }
  100% {
    width: 100px;
    height: 100px;
    opacity: 0;
  }
}
</style>