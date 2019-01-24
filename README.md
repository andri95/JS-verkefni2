# JS-verkefni2
//
let breakfast = {
    name: "The Lumberjack",
    price: "$9.95",
    ingredients: ["eggs", "sausage", "toast", "hashbrowns", "pancakes"]
};

//
var savingsAccount = {
    balance: 1000,
    interestRatePercent: 1,
    deposit: function addMoney(amount) {
        if (amount > 0) {
            savingsAccount.balance += amount;
        }
    },
    withdraw: function removeMoney(amount) {
        var verifyBalance = savingsAccount.balance - amount;
        if (amount > 0 && verifyBalance >= 0) {
            savingsAccount.balance -= amount;
        }
    },
    printAccountSummary: function (){
        return "Welcome!\nYour balance is currently $" + this.balance + " and your interest rate is " + this.interestRatePercent +"%.";
    }
};

console.log(savingsAccount.printAccountSummary());

//
var donuts = [
    { type: "Jelly", cost: 1.22 },
    { type: "Chocolate", cost: 2.45 },
    { type: "Cider", cost: 1.59 },
    { type: "Boston Cream", cost: 5.99 }
];

// your code goes here


donuts.forEach(function(skrifaUt){
    console.log(skrifaUt.type + " donuts cost $" + skrifaUt.cost + " each")
});

8. 
Samkvæmt javascript.info eru eigindi í sömu röð og þau eru sett inn. Undantekningin er ef eigindin eru integer eigindi, þá er þeim raðað eftir stærð. Ekki er þeim þó raðað eins allstaðar. Tekið er fram að í USA kemur 1 fyrst en í Austurríki kemur hæsta tala fyrst.

9. 
Hér er notandi að copy-a objectinn user inn í breytuna admin. Þegar user er breytt breytist innihald admin og öfugt. Þó ef admin breytunni er eytt lifir user breytan ennþá. Mig minnti að þetta væri þannig að ef user er breytt breytist admin en ekki öfugt en þegar ég prufaði bæði í console breyttist á báða vegu.

10.
Const gerir það bara að verkum að "the variable identifier" (á erfitt með að koma þessu í íslensku) er ekki hægt að breyta,en það sem breytan inniheldur er hægt að breyta.
