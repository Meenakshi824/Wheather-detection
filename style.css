document.getElementById("getWeatherBtn").addEventListener("click", getWeather);

async function getWeather() {
  const location = document.getElementById("locationInput").value;
  const apiKey = "e6cfbc9926384d70933153417251509";
  const url = `http://api.weatherapi.com/v1/current.json?key=${apiKey}&q=${location}&aqi=yes`;

  try {
    const response = await fetch(url);
    if (!response.ok) {
      throw new Error("Location not found");
    }

    const data = await response.json();
    const temp = data.current.temp_c;
    const condition = data.current.condition.text;
    const city = data.location.name;
    const country = data.location.country;

    document.getElementById("result").innerHTML = `
      <strong>${city}, ${country}</strong><br>
      🌡 Temperature: ${temp} °C <br>
      ☁ Condition: ${condition}
    `;
  } catch (error) {
    document.getElementById("result").innerHTML = "❌ Error: " + error.message;
  }
}
