const suffixes = ["a", "aa", "f", "ff", "0", "00", "5", "55"];
let inputHex = prompt("Enter your HEX color (e.g., #262425ff or 262425):").replace('#', '').trim();
const fullHex = inputHex.length > 6 ? `#${inputHex}` : null;
const baseHex = inputHex.slice(0, 6);
if (!/^[0-9A-Fa-f]{6,8}$/.test(inputHex)) {
    alert("Invalid HEX! Please enter a valid 6-8 character HEX code.");
} else {
    const form = document.querySelector(".createCrewFormInner"),
          colorField = document.querySelector("#crewColor"),
          submitButton = document.querySelector("#createCrewFormBtn"),
          feedback = document.createElement("div");
    feedback.style.color = "#fff";
    feedback.style.padding = "15px";
    feedback.style.marginBottom = "5px";
    feedback.style.background = "rgb(0,50,150)";
    form.insertBefore(feedback, form.firstChild);
    let attempt = 0;
    function tryColor(hex) {
        feedback.textContent = `Trying: ${hex}...`;
        if (colorField && submitButton) {
            colorField.value = hex;
            submitButton.click();
            setTimeout(() => {
                if (document.querySelector(".actions p.success")) {
                    feedback.style.background = "rgb(0,150,100)";
                    feedback.textContent = `Success! Color set to ${hex}.`;
                    document.querySelector(".minicolors-swatch-color").style.background = hex;
                } else if (attempt < suffixes.length) {
                    tryColor(`#${baseHex}${suffixes[attempt++]}`);
                } else {
                    feedback.style.background = "rgb(150,10,10)";
                    feedback.textContent = "Failed to set color with any combination.";
                }
            }, 1000);
        }
    }
    if (fullHex) {
        tryColor(fullHex);
    } else {
        tryColor(`#${baseHex}`);
    }
}
