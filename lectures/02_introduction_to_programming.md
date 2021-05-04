---
title: 02. პროგრამირების საფუძვლები
parent: ლექციები
---

პირველ კვირას გავეცანით 


> გაითვალისწინეთ: ამ ლექციაში ბევრი ახალი ტერმინი იქნება. არ მოგეთხოვებათ ყველაფერი მალევე გახსოვდეთ, მთელი სემესტრის განმავლობაში გავიმეორებთ ხოლმე და მაგალითების საფუძველზე ისწავლით, მერე გამოცდამდე გაიმეორებთ. ახლა დაჯდომა და დაზეპირება არ დაიწყოთ.

# პროგრამირების სტრუქტურები
თითოეულის სათაურის ქვემოთ დალინკულია შესაბამისი ვიდეო [მეორე კვირის](https://codehs.com/lms/assignment/43749489) მასალიდან
## ფუნქციები
<https://codehs.com/lms/assignment/41699430/>
შეგვიძლია კარელს (ან ნებისმიერ პროგრამას) ვასწავლოთ ახალი ბრძანება (არსებული ბრძანებების ერთობლიობას დავარქვათ სახელი და ის გამოვიყენოთ)

```js
function turnAround() {
    turnLeft();
    turnLeft();
}
```

### კოდის ბლოკი {}
ფიგურული ფრჩხილებით შემოფარგლული ხაზები, რომლებიც მიეკუთვნება კონკრეტულ პროგრამულ სტრუქტურას (მაგალითად, ფუნქციას). 

## ფაილის სტრუქტურა
### კომენტარები
კოდი, რომელსაც პროგრამა დააიგნორებს. შეგვიძლია გამოვიყენოთ ახსნების დასამატებლად. 
```js
takeBall(); // ერთხაზიანი კომენტარი. 

/*
რამდენიმე ხაზიანი კომენტარი
მაგალითად ფუნქციის წინ ამ ფუნქციის ახსნის დასაწერად
*/
```
### ინდენტაცია
კოდის ბლოკებს ფუნქციების გარდა სხვა სტრუქტურებიც იყენებენ და ჩვენ შეგვიძლია ამ სტრუქტურების კომბინაცია (ერთ ბლოკში მეორის გახსნა და ა.შ). მნიშვნელოვანია, რომ ამ დროს დაიცვათ ინდენტაცია და ყოველი ახალი ბლოკის ხაზები შეწეული იყოს `tab`-ით
```js
function f1() {
    somecode(); // შეწიე ერთი tab-ით. 
    if (somethingTrue()) {
        doStuff(); // შეწიე კიდევ ერთი tab-ით
    }
    someOtherCode();
}
```

## კონტროლის სტრუქტურები
### გამეორება - for loop
<https://codehs.com/lms/assignment/41699465/>
თუ გვინდა კარელმა რამე ბრძანება (ან ბრძანებები) N-ჯერ გაიმეოროს, ამ რიცხვს ვწერთ ასეთ სტრუქტურაში. ახლა იქნება პირველი შემთხვევა, როცა გეტყვით რომ რაღაც ნაწილს არ მიაქციოთ ყურადღება როგორ მუშაობს. ზედმეტი ინფორმაციის გაფილტვრა არის უნარი, რომელიც გეხმარებათ გააკეთოთ მეტი პროგრესი და მოგვიანებით მოუბრუნდეთ რთულ ნაწილებს. ასევე მნიშვნელოვანია ის, რომ პროგრესის შემდეგ მეტი შანსი გაქვთ ეს რთული ნაწილი გაიგოთ, რადგან უკვე მეტი გამოცდილება გაქვთ. უბრალოდ დაიმახსოვრეთ, რომ შუა რიცხვი უნდა შეცვალოთ.
```js
for (var i=0; i < 9; i++) {
    move(); // გადავა 9-ჯერ
}
```

გამეორების საშუალება ბევრ საქმეს გვიმარტივებს, მაგრამ ამ შემთხვევაშიც კი ჩვენს პროგრამას არანაირი ინტელექტი არ აქვს. შეუძლია შეასრულოს მშრალად დაწერილი ბრძანებები ერთმანეთის მიყოლებით, მაგრამ მას არ აქვს გადაწყვეტილების მიღების შესაძლებლობა.

### პირობის შემოწმება - if/else statement
<https://codehs.com/lms/assignment/41699479/>
```js
if (somethingTrue()) {
    doStuff();
} else {
    doAnotherStuff();
}
```

### პირობის საფუძველზე გამეორება - while loop
<https://codehs.com/lms/assignment/41699496/>
```js
while (somethingTrue()) {
    keepDoingStuff()
}
```

# პრობლემებთან/ამოცანებთან მუშაობის პრინციპები
პროგრამირება არ არის გაუჩერებლად კლავიატურაზე კაკუნი და ენთერის შემდეგ შედეგის მიღება - პროგრამირება არის **ფიქრის პროცესი**. ეს არის სტრატეგიების და (გამომუშავებადი) უნარების ერთობლიობა, რომელსაც იყენებ სხვადასხვა პრობლემებთან (არა მხოლოდ კოდის) გასამკლავებლად.


## დეკომპოზიცია
დიდი და კომპლექსური პრობლემა შეიძლება უფრო მარტივი იყოს, თუ პრობლემების იზოლირებას და დაყოფას შევეცდებით.

## აბსტრაქცია
სირთულეებთან გამკლავება არაგადამწყვეტი დეტალების დამალვით. **შავი ყუთის პრინციპი**. 

ჩვენ ვიყენებთ ფუნქციას `move()`, მაგრამ არ ვღელავთ იმაზე, თუ როგორ იწვევს ამ ფუნქციის გამოყენება კარელის გადაადგილებას სამყაროში. ვიცით ის, რომ თუ კარელი დგას x უჯრაზე, move()-ის გამოძახების შემდეგ იდგება მის შემდეგ უჯრაზე. ეს ორი (საწყისი და საბოლოო პოზიცია) არის შავი ყუთის input და output.

აბსტრაქცია მხოლოდ სხვის მიერ შექმნილ კოდზე არ ვრცელდება. მუშაობისას მნიშვნელოვანია რომ ვიყოთ კონცენტრირებული **მხოლოდ ერთ და მარტივ** პრობლემაზე. ეს ნიშნავს, რომ ჩვენივე პასუხისმგებლობაა ამისთვის საჭირო გარემოს მომზადება (სხვა ფუნქციების შექმნა ისე, რომ მერე მათზე ფიქრის გარეშე გამოვიყენოთ)


## ალგორითმის დიზაინი
### top down
დეკომპოზიციის ბუნებრივი შედეგი არის ის, რომ საბოლოო ჯამში გვაქვს პატარ-პატარა პრობლემები. ჩვენ ჯერ ამ პრობლემებს გავუმკლავდებით და შემდეგ დავაკავშირებთ ერთმანეთს მომდევნო საფეხურებზე. 

### bottom up
უფრო ხშირად ვიდრე არა, ასე სრულყოფილი დეკომპოზიცია შეუძლებელია. ზოგჯერ შეიძლება ერთი ქვეპრობლემის ამოხსნამ უკეთესი წარმოდგენა მოგვცეს იმაზე, როგორ შეიძლება დავუკავშიროთ იგი სხვებს.

## პასუხისმგებლობების განაწილება
ამ პრინციპების კოდში დაცვისთვის
- ერთი ფუნქცია უნდა ასრულებდეს ერთ კონკრეტულ დავალებას
- მარტივი უნდა იყოს ფუნქციის მუშაობის აღწერა (x input-ზე არის y output). დაწერეთ ეს აღწერა კომენტარად ფუნქციის დასაწყისში
- ფუნქცია არ უნდა იყოს გრძელი - თუ 5-6 ხაზს გადააჭარბებს, დაფიქრდით ხომ არ შეიძლება რამე ნაწილის გატანა სხვა ფუნქციაში
- თუ ორ ფუნქციას მსგავსი კოდი აქვს, საერთო ნაწილები გაიტანეთ ცალკე ფუნქციად.

## მსგავსებების ამოცნობა (pattern recognition)
გამოყენებადი ბლოკების შექმნა. აბსტრაქციების გამოყენებადობა პირდაპირ კავშირშია მათ რაოდენობასთან - ძალიან ბევრი თუ იყო შეიძლება არ გაგახსენდეთ, ან თავიდან შექმნათ თითქმის იმავენაირი აბსტრაქცია. ამიტომ მნიშვნელოვანია დააკვირდეთ მსგავს კოდებს და 

## ამ უნარების ათვისება
მიუხედავად იმისა, რომ ეს პრინციპები ყოველდღიური ცხოვრების ნაწილია, მათი გამიზნულად და გაცნობიერებლად გამოყენება დაკვირვებით ვარჯიშს მოითხოვს. თავიდან თუ არ გამოგივათ, ხელი არ ჩაიქნიოთ - ზოგჯერ პრობლემაზე მუშაობის დასრულების შემდეგ შეიძლება აღიქვათ როგორი იქნებოდა სწორი დეკომპოზიცია, ან ნაწილებზე top down-ით იმუშაოთ, სხვაზე bottom up-ით და ასე არეულად. მთავარია შეეცადოთ, დააკვირდეთ და ყველა მცირე წარმატება დააფასოთ.


