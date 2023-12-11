let money = 0;
let isSmaller = false;
const runing = true;
const brokerButtonContainer = document.getElementById("buyBrokerButton");
const calculatorButtonContainer = document.getElementById("buyCalculatorButton");
const shopButtonContainer = document.getElementById("buyShopButton");
const factoryButtonContainer = document.getElementById("buyFactoryButton");
const bankButtonContainer = document.getElementById("buyBankButton");
const printerButtonContainer = document.getElementById("buyPrinterButton");
const labaratoryButtonContainer = document.getElementById("buyLabaratoryButton");
const portalButtonContainer = document.getElementById("buyPortalButton");
const timeTravellerButtonContainer = document.getElementById("buyTimeTravellerButton");
const quantumComputerButtonContainer = document.getElementById("buyQuantumComuterButton");

let cursor = {
    name: 'Cursor',
    price: 40,
    moneyPerSecond: 1,
    displayButton: true,
    amount: 0
}

let broker = {
    name: 'Broker',
    price: 100,
    moneyPerSecond: 4,
    displayButton: false,
    amount: 0
}

let calculator = {
    name: 'Calculator',
    price: 1000,
    moneyPerSecond: 40,
    displayButton: false,
    amount: 0
}

let shop = {
    name: 'Shop',
    price: 10000,
    moneyPerSecond: 400,
    displayButton: false,
    amount: 0
}

let factory = {
    name: 'Factory',
    price: 100000,
    moneyPerSecond: 4000,
    displayButton: false,
    amount: 0
}

let bank = {
    name: 'Bank',
    price: 1000000,
    moneyPerSecond: 40000,
    displayButton: false,
    amount: 0
}

let printer = {
    name: 'Printer',
    price: 2000000,
    moneyPerSecond: 40000,
    displayButton: false,
    amount: 0
}

let laboratory = {
    name: 'Laboratory',
    price: 5000000,
    moneyPerSecond: 400000,
    displayButton: false,
    amount: 0
}

let portal = {
    name: 'Portal',
    price: 10000000,
    moneyPerSecond: 400000,
    displayButton: false,
    amount: 0
}

let timeTraveller = {
    name: 'Time traveller',
    price: 20000000,
    moneyPerSecond: 450000,
    displayButton: false,
    amount: 0
}

let quantumComputer = {
    name: 'Quantum computer',
    price: 50000000    moneyPerSecond: 200000,
    displayButton: false,
    amount: 0
    }
    
    let matrica = {
    name: 'matrica',
    price: 690000000   moneyPerSecond: 6900000
    displayButton: false,
    amount: 0
}

function calculateAndAddMoneyPerSecond() {
    moneyPerSecond = cursor.moneyPerSecond * cursor.amount + broker.moneyPerSecond * broker.amount + calculator.moneyPerSecond * calculator.amount + shop.moneyPerSecond * shop.amount + factory.moneyPerSecond * factory.amount + bank.moneyPerSecond * bank.amount + printer.moneyPerSecond * printer.amount + labaratory.moneyPerSecond * labaratory.amount + portal.moneyPerSecond * portal.amount + timeTraveller.moneyPerSecond * timeTraveller.amount + quantumComputer.moneyPerSecond * quantumComputer.amount;
    money = money + moneyPerSecond;
    updateDisplay()
}

function addMoney(moneyAmount) {
    money = money + moneyAmount;
    updateDisplay()
}

function toggleSize() {
    const image = document.getElementById('Coin');
    if (isSmaller) {
        image.style.transform = 'scale(1.0)';
    } else {
        image.style.transform = 'scale(0.9)';
    }

    isSmaller = !isSmaller;
}

function toggleBrokerButtonVisibility() {
    if (broker.displayButton === true) {
        brokerButtonContainer.style.display = "block";
    } else {
        brokerButtonContainer.style.display = "none";
    }
}

function toggleCalculatorButtonVisibility() {
    if (calculator.displayButton === true) {
        calculatorButtonContainer.style.display = "block";
    } else {
        calculatorButtonContainer.style.display = "none";
    }
}

function toggleShopButtonVisibility() {
    if (shop.displayButton === true) {
        shopButtonContainer.style.display = "block";
    } else {
        shopButtonContainer.style.display = "none";
    }
}

function toggleFactoryButtonVisibility() {
    if (factory.displayButton === true) {
        factoryButtonContainer.style.display = "block";
    } else {
        factoryButtonContainer.style.display = "none";
    }
}

function toggleBankButtonVisibility() {
    if (bank.displayButton === true) {
        bankButtonContainer.style.display = "block";
    } else {
        bankButtonContainer.style.display = "none";
    }
}

function togglePrinterButtonVisibility() {
    if (printer.displayButton === true) {
        printerButtonContainer.style.display = "block";
    } else {
        printerButtonContainer.style.display = "none";
    }
}


function buyCursor() {
    if (money >= cursor.price) {
        money = money - cursor.price;
        cursor.amount++;
    }
    updateDisplay()
}

function buyBroker() {
    if (money >= broker.price) {
        money = money - broker.price;
        broker.amount++;
    }
    updateDisplay()
}

function buyCalculator() {
    if (money >= calculator.price) {
        money = money - calculator.price;
        calculator.amount++;
    }
    updateDisplay()
}
function buyShop() {
    if (money >= shop.price) {
        money = money - shop.price;
        shop.amount++;
    }
    updateDisplay()
}

function buyFactory() {
    if (money >= factory.price) {
        money = money - factory.price;
        factory.amount++;
    }
    updateDisplay()
}

function buyBank() {
    if (money >= bank.price) {
        money = money - bank.price;
        bank.amount++;
    }
    updateDisplay()
}

function buyPrinter() {
    if (money >= printer.price) {
        money = money - printer.price;
        printer.amount++;
    }
    updateDisplay()
}

function buyLabaratory() {
    if (money >= labaratory.price) {
        money = money - labaratory.price;
        labaratory.amount++;
    }
    updateDisplay()
}

function buyPortal() {
    if (money >= portal.price) {
        money = money - portal.price;
        portal.amount++;
    }
    updateDisplay()
}

function buyTimeTraveller() {
    if (money >= timeTraveller.price) {
        money = money - timeTraveller.price;
        timeTraveller.amount++;
    }
    updateDisplay()
}

function buyQuantumComputer() {
    if (money >= quantumComputer.price) {
        money = money - quantumComputer.price;
        quantumComputer.amount++;
    }
}

function updateDisplay() {
    document.getElementById("moneyCount").innerHTML = money;
    document.getElementById("moneyPerSecond").innerHTML = moneyPerSecond;
    document.getElementById("cursor").innerHTML = cursor.amount;
    document.getElementById("broker").innerHTML = broker.amount;
    document.getElementById("calculator").innerHTML = calculator.amount;
    document.getElementById("shop").innerHTML = shop.amount;
    document.getElementById("factory").innerHTML = factory.amount;
    document.getElementById("bank").innerHTML = bank.amount;
    document.getElementById("printer").innerHTML = printer.amount;
    document.getElementById("labaratory").innerHTML = labaratory.amount;
    document.getElementById("portal").innerHTML = portal.amount;
    document.getElementById("time traveller").innerHTML = timeTraveller.amount;
    document.getElementById("quantum computer").innerHTML = quantumComputer.amount;
    toggleBrokerButtonVisibility()
    toggleCalculatorButtonVisibility()
    toggleShopButtonVisibility()
    toggleFactoryButtonVisibility()
    toggleBankButtonVisibility()
    togglePrinterButtonVisibility()
}

while (money != broker.price) {
    if (money >= broker.price) {
        broker.displayButton = true;
    } else {
        broker.displayButton = false;
    }
}

while (money != calculator.price) {
    if (money >= calculator.price) {
        calculator.displayButton = true;
    } else {
        calculator.displayButton = false;
    }
}

while (money != shop.price) {
    if (money >= shop.price) {
        shop.displayButton = true;
    } else {
        shop.displayButton = false;
    }
}

while (money != factory.price) {
    if (money >= factory.price) {
        factory.displayButton = true;
    } else {
        factory.displayButton = false;
    }
}



setInterval(calculateAndAddMoneyPerSecond, 1000)
updateDisplay()
