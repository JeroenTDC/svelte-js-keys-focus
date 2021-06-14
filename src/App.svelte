<script>
document.addEventListener('keydown', logKey);
document.addEventListener('mousedown', getFocus);

function getFocus() {
    var mainElement = document.getElementById("main");
    var isFocused = (document.getElementById("main").hasFocus());

    console.log(isFocused);
}

function logKey(e) {
    var mainElement = document.getElementById("main");

    if (e.code === 'Escape') {
        //alert('escape pressed')
        log.textContent += ` ${e.code}`;
        mainElement.style.color = "white";
    }

    switch (e.code) {
        case 'Escape':
            mainElement.style.display = "none";
            break;
        case 'KeyB':
            mainElement.style.color = "blue";
            break;
        case 'KeyO':
            mainElement.style.color = "orange";
            break;
        case 'KeyP':
            mainElement.style.color = "pink";
            break;
        case 'KeyG':
            mainElement.style.color = "green";
            break;
    }
}
</script>

<main id="main">
    <p>Focus the IFrame first (e.g. by clicking in it), then try pressing some keys.</p>
    <p id="log"></p></main>

<style>
main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
}

h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
}

@media (min-width: 640px) {
    main {
        max-width: none;
    }
}
</style>
