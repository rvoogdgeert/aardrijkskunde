<script lang="ts">
    import FlashCard from "./lib/FlashCard.svelte";

    // Define flash cards data structure
    const flashCards = [
        {
            id: 1,
            question:
                "Schokkende beweging van een gedeelte van de aardkorst door de werking van endogene krachten.",
            answer: "aardbeving",
        },
        {
            id: 2,
            question: "Plaat die bestaat uit een groot landoppervlak.",
            answer: "continentale plaat",
        },
        {
            id: 3,
            question:
                "Stroming van het gesmolten gesteente onder de aardkorst binnen in de aarde.",
            answer: "convectiestromen",
        },
        {
            id: 4,
            question: "Heet vloeibaar gesteente binnen in de aarde.",
            answer: "magma",
        },
        {
            id: 5,
            question: "Magma dat door de aardkorst naar buiten is gestroomd.",
            answer: "lava",
        },
        {
            id: 6,
            question: "Plaat die bestaat uit een groot zeeoppervlak.",
            answer: "oceanische plaat",
        },
        {
            id: 7,
            question:
                "Een ramp veroorzaakt door de natuur met veel slachtoffers en grote schade.",
            answer: "natuurramp",
        },
        {
            id: 8,
            question: "Stuk van de aardkorst.",
            answer: "plaat",
        },
        {
            id: 9,
            question:
                "Schaal die de hevigheid en de schade een aardbeving weergeeft.",
            answer: "schaal van Mercalli",
        },
        {
            id: 10,
            question: "Een ander woord voor platen.",
            answer: "schollen",
        },
        {
            id: 11,
            question:
                "Het wegduiken van een oceanische plaat onder een continentale plaat.",
            answer: "subductie",
        },
        {
            id: 12,
            question:
                "Een diepe kloof in de oceaan die onstaat door subductie van een oceanische plaat.",
            answer: "trog",
        },
        {
            id: 13,
            question:
                "Berg die ontstaan is door het naar buiten stromen van lava.",
            answer: "vulkaan",
        },
        {
            id: 14,
            question:
                "Dunne laag gesteente om de aarde met een dikte van gemiddeld 8 km onder oceanen en 35 km onder continenten.",
            answer: "aardkorst",
        },
        {
            id: 15,
            question: "Barst of scheur in de aardkorst.",
            answer: "breuk",
        },
        {
            id: 16,
            question: "Het naar elkaar toedrijven van platen.",
            answer: "convergentie",
        },
        {
            id: 17,
            question: "Het uitelkaar drijven van platen.",
            answer: "divergentie",
        },
        {
            id: 18,
            question: "Kracht die van binnenuit de aardkorst verandert.",
            answer: "endogene kracht",
        },
        {
            id: 19,
            question: "Kracht die van buitenaf de aardkorst verandert.",
            answer: "exogene kracht",
        },
        {
            id: 20,
            question:
                "Langrekte bergrug onder in de zee, ontstaan doordat magma bij het uitelkaar drijven van oceanische platen naar boven komt.",
            answer: "mid-oceanische rug",
        },
        {
            id: 21,
            question: "Het langs elkaar bewegen van platen.",
            answer: "transforme beweging",
        },
        {
            id: 22,
            question: "Stuk van de aardkorst.",
            answer: "plaat",
        },
        {
            id: 23,
            question: "Een gebied verlaten omdat het er niet meer veilig is.",
            answer: "evacueren",
        },
        {
            id: 24,
            question:
                "Schaal waarmee de kracht van een aardbeving wordt gemeten.",
            answer: "schaal van Richter",
        },
        {
            id: 25,
            question:
                "Hoge vloedgolf op de zee die de kust overspoelt en die wordt veroorzaakt door een zeebeving.",
            answer: "tsunami",
        },
        {
            id: 26,
            question: "Aardbeving waarvan het epicentrum in de zee ligt.",
            answer: "zeebeving",
        },
        {
            id: 27,
            question:
                "Het punt waar de aardbeving aan de aardoppervlakte komt, direct boven het hypocentrum.",
            answer: "epicentrum",
        },
        {
            id: 28,
            question: "Plaats die in de aardkorst waar de aardbeving begint.",
            answer: "hypocentrum",
        },
        {
            id: 29,
            question:
                "De schaal waarop je naar de wereld kijkt: lokaal, regionaal, nationaal, continentaal, of mondiaal.",
            answer: "schaalniveau",
        },
        {
            id: 30,
            question:
                "Wetenschapper die zich bezighoudt met het bestuderen van aardbevingen.",
            answer: "seismoloog",
        },
        {
            id: 31,
            question:
                "Zeer grote vulkaankrater die is ontstaan door het instorten van het dak van een leeggelopen magmakamer.",
            answer: "caldeira",
        },
        {
            id: 32,
            question: "Aardwarmte.",
            answer: "geothermie",
        },
        {
            id: 33,
            question:
                "Hete gassen vermengd met stenen en as die bij een vulkaanuitbarsting de helling afrazen. Heet ook gloedwolk.",
            answer: "pyroclastische stroom",
        },
        {
            id: 34,
            question:
                "Bron die ontstaat door geothermische verwarming van grondwater. Heet ook hot spring.",
            answer: "warmtebron",
        },
        {
            id: 35,
            question: "Ruimte in een vulkaan die gevuld is met magma.",
            answer: "magmakamer",
        },
        {
            id: 36,
            question:
                "Vrij zachte steensoort die bestaat uit aan elkaar gekitte vulkanische as.",
            answer: "tufsteen",
        },
        {
            id: 37,
            question:
                "Oude vulkaan met een grote kilometersbrede krater door het leeglopen van de magmakamer waardoor het dak ervan is instort.",
            answer: "caldeiravulkaan",
        },
        {
            id: 38,
            question:
                "Oude vulkaan met een grote kilometersbrede krater door het leeglopen van de magmakamer waardoor het dak ervan is instort.",
            answer: "caldeiravulkaan",
        },
        {
            id: 39,
            question: "vulkaanuitbarsting.",
            answer: "eruptie",
        },
        {
            id: 40,
            question:
                "Grot gat met steile wanden dat ontstaat tijdens een vulkaanuitbarsting.",
            answer: "krater",
        },
        {
            id: 41,
            question: "Meer dat is ontstaan door het vollopen van een krater.",
            answer: "kratermeer",
        },
        {
            id: 42,
            question:
                "Vulkanisch verschijnsel dat voorkomt bij een vulkaan die niet meer actief is.",
            answer: "postvulkanisch verschijnsel",
        },
        {
            id: 43,
            question: "Lage brede vulkaan met flauwe hellingen.",
            answer: "schildvulkaan",
        },
        {
            id: 44,
            question:
                "Vulkaan met steile hellingen die opgebouwd is uit lagen lava en pyroclastisch materiaal.",
            answer: "stratovulkaan",
        },
    ];

    // Create a shuffled version of the flashcards
    let shuffledCards = [];

    // Fisher-Yates shuffle algorithm function
    function shuffleArray(array: any) {
        // Create a copy of the original array to avoid modifying it
        const arrayCopy = [...array];
        // Start from the last element and swap it with a randomly selected element
        for (let i = arrayCopy.length - 1; i > 0; i--) {
            // Pick a random index from 0 to i
            const j = Math.floor(Math.random() * (i + 1));
            // Swap elements at i and j
            [arrayCopy[i], arrayCopy[j]] = [arrayCopy[j], arrayCopy[i]];
        }
        return arrayCopy;
    }

    // Initialize shuffled cards when component loads
    shuffledCards = shuffleArray(flashCards);

    // Keep track of the current card index
    let currentCardIndex = 0;

    // State for tracking points system
    let points = 0;
    let attempted = 0;

    // Function to go to the next card
    // Function to go to the next card
    function nextCard() {
        if (currentCardIndex < shuffledCards.length - 1) {
            currentCardIndex++;
        }
    }

    // Function to go to the previous card
    function prevCard() {
        if (currentCardIndex > 0) {
            currentCardIndex--;
        }
    }
    // Function to update points when an answer is submitted
    function handleAnswerSubmit(event: any) {
        const isCorrect = event.detail.isCorrect;
        attempted++;

        if (isCorrect) {
            points++; // Add 1 point for correct answer

            // Set a 2-second delay for correct answers before moving to the next card
            if (currentCardIndex < shuffledCards.length - 1) {
                setTimeout(() => {
                    nextCard();
                }, 2000);
            }
        } else {
            // No point deduction for incorrect answers

            // Set a 5-second delay for incorrect answers before moving to the next card
            if (currentCardIndex < shuffledCards.length - 1) {
                setTimeout(() => {
                    nextCard();
                }, 5000);
            }
        }
    }
</script>

<main>
    <div class="container">
        <h1>Flash Cards Aardrijkskunde</h1>

        <div class="score-container">
            <p>Points: {points} (Attempted: {attempted})</p>
        </div>

        <div class="card-container">
            <FlashCard
                flashCard={shuffledCards[currentCardIndex]}
                on:answerSubmitted={handleAnswerSubmit}
            />
        </div>

        <div class="navigation">
            <button on:click={prevCard} disabled={currentCardIndex === 0}
                >Previous</button
            >
            <span class="card-counter"
                >{currentCardIndex + 1} / {shuffledCards.length}</span
            >
            <button
                on:click={nextCard}
                disabled={currentCardIndex === shuffledCards.length - 1}
                >Next</button
            >
        </div>
    </div>
</main>

<style>
    :global(body) {
        background-color: #10abb4;
        color: #004c50;
        margin: 0;
        padding: 0;
        font-family:
            -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen-Sans,
            Ubuntu, Cantarell, "Helvetica Neue", sans-serif;
    }

    .container {
        display: flex;
        flex-direction: column;
        align-items: center;
        max-width: 800px;
        margin: 0 auto;
        padding: 20px;
        background-color: white;
        border-radius: 12px;
        box-shadow: 0 4px 12px rgba(0, 76, 80, 0.1);
    }

    h1 {
        color: #004c50;
        margin-bottom: 20px;
        font-weight: 700;
        text-align: center;
    }

    .score-container {
        margin-bottom: 20px;
        font-size: 1.2rem;
        font-weight: bold;
        color: #004c50;
        background-color: rgba(16, 171, 180, 0.1);
        padding: 8px 16px;
        border-radius: 8px;
    }

    .card-container {
        width: 100%;
        margin-bottom: 20px;
    }

    .navigation {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 100%;
        max-width: 400px;
        padding: 10px;
        background-color: rgba(0, 147, 156, 0.05);
        border-radius: 8px;
    }

    button {
        background-color: #00939c;
        color: white;
        border: none;
        padding: 10px 20px;
        text-align: center;
        text-decoration: none;
        display: inline-block;
        font-size: 16px;
        margin: 4px 2px;
        cursor: pointer;
        border-radius: 4px;
        transition: all 0.3s ease;
        font-weight: 500;
        box-shadow: 0 2px 4px rgba(0, 76, 80, 0.2);
    }

    button:hover {
        background-color: #10abb4;
        transform: translateY(-2px);
        box-shadow: 0 4px 8px rgba(0, 76, 80, 0.3);
    }

    button:disabled {
        background-color: rgba(0, 147, 156, 0.3);
        cursor: not-allowed;
        box-shadow: none;
        transform: none;
    }

    .card-counter {
        font-size: 1rem;
        color: #502000;
        font-weight: 600;
        background-color: rgba(156, 62, 0, 0.1);
        padding: 4px 10px;
        border-radius: 4px;
    }
</style>
