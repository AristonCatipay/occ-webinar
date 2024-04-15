```js
const cards = [
    "The Fool", "The Magician", "The High Priestess", "The Empress", "The Emperor", "The Hierophant", "The Lovers", "The Chariot", "Strength", "The Hermit"
    // Add more cards here
];


const interpretations = {
    "The Fool": "Embark on a new journey with enthusiasm and an open heart. Embrace the unknown and take risks, for they may lead to unexpected rewards. Trust your instincts and follow your inner calling.",
    "The Magician": "Harness your inner power to manifest your desires. You possess the tools needed to turn your ideas into reality. Tap into your resourcefulness and take deliberate action to achieve your goals.",
    "The High Priestess": "Listen to your intuition and explore the depths of your subconscious mind. Secrets and mysteries surround you – trust your inner wisdom to guide you through the shadows. Seek hidden knowledge and embrace your intuitive insights.",
    "The Empress": "Nurture and care for your creative projects and relationships, for they have the potential to flourish. Abundance and fertility are at your doorstep. Embrace the beauty of nature and the joy of creation.",
    "The Emperor": "Step into a role of leadership and authority. Provide structure and guidance for yourself and others. Uphold discipline and order while maintaining your ambition. Your steady presence will create a foundation for success.",
    "The Hierophant": "Embrace tradition and explore your spirituality. Seek wisdom from established teachings while remaining open to your unique spiritual path. Conformity can offer comfort, but be mindful to balance it with personal growth.",
    "The Lovers": "Experience deep emotional connections and harmony in your relationships. Explore the balance between your heart and mind. Choices made from a place of love and authenticity will lead to fulfillment.",
    "The Chariot": "Harness your determination and willpower to overcome obstacles on your journey. Stay focused and drive forward with confidence. Success comes through discipline and the ability to navigate challenges.",
    "Strength": "Tap into your inner strength and courage to face challenges with grace. Patience and resilience will lead to triumph. Embrace your wild and gentle side, finding balance in your interactions.",
    "The Hermit": "Embark on a journey of self-discovery and introspection. Seek solitude to connect with your inner guidance and illuminate your path. Trust your inner wisdom and allow it to guide you to deeper understanding."
    // Add more expanded interpretations here
};


const cardImages = {
    "The Fool": "https://www.biddytarot.com/wp-content/uploads/2018/02/0-fool-345x480.png", // Replace with actual image paths
    "The Magician": "https://www.biddytarot.com/wp-content/uploads/2018/02/01-magician-345x480.png",
    "The High Priestess": "https://www.biddytarot.com/wp-content/uploads/2018/02/02-highpriestess-345x480.png",
    "The Empress": "https://www.biddytarot.com/wp-content/uploads/2018/02/03-empress-345x480.png",
    "The Emperor": "https://www.biddytarot.com/wp-content/uploads/2018/02/04-emperor-345x480.png",
    "The Hierophant": "https://www.biddytarot.com/wp-content/uploads/2018/02/05-hierophant-345x480.png",
    "The Lovers": "https://www.biddytarot.com/wp-content/uploads/2018/02/06-lovers.png",
    "The Chariot": "https://www.biddytarot.com/wp-content/uploads/2018/02/07-chariot-345x480.png",
    "Strength": "https://www.biddytarot.com/wp-content/uploads/2018/02/08-strength-345x480.png",
    "The Hermit": "https://www.biddytarot.com/wp-content/uploads/2018/02/09-hermit-345x480.png",
  
};


const drawButton = document.getElementById("drawButton");
const cardDisplay = document.getElementById("cardDisplay");
const interpretationDisplay = document.getElementById("interpretation");


drawButton.addEventListener("click", drawCard);


function drawCard() {
    const randomIndex = Math.floor(Math.random() * cards.length);
    const drawnCard = cards[randomIndex];
    const interpretation = interpretations[drawnCard] || "No interpretation available.";
    const cardImagePath = cardImages[drawnCard] || ""; // Default image


    cardDisplay.textContent = `You drew: ${drawnCard}`;
    interpretationDisplay.textContent = `Interpretation: ${interpretation}`;
    cardDisplay.style.backgroundImage = `url('${cardImagePath}')`;
}
```