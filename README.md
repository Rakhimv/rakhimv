### Hi there 👋

# Таймер

Оставшееся время: <span id="timer"></span>

<script>
// Устанавливаем дату окончания таймера (например, через 1 час)
const endDate = new Date();
endDate.setHours(endDate.getHours() + 1);

// Функция для обновления таймера
function updateTimer() {
    const now = new Date();
    const diff = Math.floor((endDate - now) / 1000); // Разница в секундах

    if (diff <= 0) {
        document.getElementById('timer').textContent = 'Таймер завершен!';
        return;
    }

    const hours = Math.floor(diff / 3600);
    const minutes = Math.floor((diff % 3600) / 60);
    const seconds = diff % 60;

    // Форматируем вывод таймера
    const timerString = `${hours.toString().padStart(2, '0')}:${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;
    document.getElementById('timer').textContent = timerString;

    // Обновляем таймер каждую секунду
    setTimeout(updateTimer, 1000);
}

// Запускаем таймер при загрузке страницы
document.addEventListener('DOMContentLoaded', updateTimer);
</script>
<h3 align="left">Languages and Tools:</h3>
<p align="left"> <a href="https://www.w3schools.com/css/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" alt="css3" width="40" height="40"/> </a> <a href="https://firebase.google.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/firebase/firebase-icon.svg" alt="firebase" width="40" height="40"/> </a> <a href="https://www.w3.org/html/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" alt="html5" width="40" height="40"/> </a> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="javascript" width="40" height="40"/> </a> <a href="https://sass-lang.com" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/sass/sass-original.svg" alt="sass" width="40" height="40"/> </a> </p>
