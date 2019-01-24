# JS-verkefni2

**1. Búðu til object með upplýsingar um þig...**
```javascript
let einstaklingur = {
    nafn: "Andri Fannar Pétursson",
    kennitala: "010695-2799",
    heimilisfang: "Blómahæð 10",
    heimasimi: "565-8108",
    gsm: "786-0068"
};
```
**2. Notaðu for..in lykkjuna til að birta öll eigindin**
```javascript
for (let key in einstaklingur){
    if(einstaklingur.hasOwnProperty(key)){
        console.log(key + " >> " + einstaklingur[key])
    }
};
```
**3. Bættu aðferð í objectið sem skilar streng með nafni og aldri**
```javascript
let einstaklingur = {
    nafn: "Andri Fannar Pétursson",
    kennitala: "010695-2799",
    heimilisfang: "Blómahæð 10",
    heimasimi: "565-8108",
    gsm: "786-0068",
    nafnAldur: function (){
        return this.nafn + " Aldur >> 23";
    }
};

einstaklingur.nafnAldur();
```
**4. Prentaðu út Nonni með console.log()**
```javascript
let family = {
    "parents":
    {
    "fathers": [{"name":"Jakob"},{"name":"Nonni"}],
    "mothers":[{"name":"Rakel"},{"name":"Sara"}]
    }
};

console.log(family.parents.fathers[1].name);
```
**5. Liður 8 í lesson 7**
```javascript
let breakfast = {
    name: "The Lumberjack",
    price: "$9.95",
    ingredients: ["eggs", "sausage", "toast", "hashbrowns", "pancakes"]
};
```
**6. liður 9 í lesson 7**
```javascript
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
```
**7. liður 12 í lesson 7**
```javascript
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
```
**8. Eru öll eigindi í sömu röð og þeim var bætt í object?**

Samkvæmt javascript.info eru eigindi í sömu röð og þau eru sett inn. Undantekningin er ef eigindin eru integer eigindi, þá er þeim raðað eftir stærð. Ekki er þeim þó raðað eins allstaðar. Tekið er fram að í USA kemur 1 fyrst en í Austurríki kemur hæsta tala fyrst.

**9. Útskýrðu hvað eftirfarandi kóði gerir:**

Hér er notandi að copy-a objectinn user inn í breytuna admin. Þegar user er breytt breytist innihald admin og öfugt. Þó ef admin breytunni er eytt lifir user breytan ennþá. Mig minnti að þetta væri þannig að ef user er breytt breytist admin en ekki öfugt en þegar ég prufaði bæði í console breyttist á báða vegu.

**10. Afhverju virkar eftirfarandi:**
Const gerir það bara að verkum að "the variable identifier" (á erfitt með að koma þessu í íslensku) er ekki hægt að breyta,en það sem breytan inniheldur er hægt að breyta.
