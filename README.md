# Event loop :arrows_counterclockwise: in JavaScript and rise of Asynchronous Behaviour.

[![Poster - HackOn](./assets/poster.jpeg)](https://www.youtube.com/watch?v=zsRv8g3C4rY)

## :red_circle: A webinar by [HackOn Hackathon](https://twitter.com/Vinit_Shahdeo/status/1251819929247993856) :rocket:

# [![YouTube Live](https://img.shields.io/badge/YouTube-Live-tomato.svg?style=for-the-badge&logo=youtube)](http://bit.ly/hackon-js) 

> ### Join at [bit.ly/hackon-js](http://bit.ly/hackon-js)

## :confused: Shall I watch?

> **That's a good question!** :raised_hand:

Do a **self analysis of your JS knowledge**, take a pause and predict the output for the below code snippet. :hushed:

If you're able to predict the correct sequence of log statements, I hope you need not watch the video, **skip to the [takeaways](#five-five-takeaways-bulb) section**. :v: **If not, do watch the [video](https://youtu.be/zsRv8g3C4rY?t=221) and thank me later! :hugs:**

<br>

```javascript
console.log('Hi!');

console.log('Hope you\'re staying safe at home!');

setTimeout(() => console.log('Turn your self isolation into self improvement!'), 1000);

setTimeout(() => console.log('Chant, Go Corona, Corona Go 😃'), 0);	

console.log('Thank You!');
```
<br>

## :five: Five Takeaways :bulb:

- JavaScript is **single threaded**, it simply means it has a **single call stack**.

- GitHub has **maximum number of pull requests in JavaScript repositories**. Check the live stats [here](https://madnight.github.io/githut/#/pull_requests/2020/1). 

- The asynchronous behaviour is not part of the JavaScript language itself, rather they are built on top of the core JavaScript language in the browser (or the programming environment) and accessed through the **browser APIs**.

- **`setTimeout(function, delay)`** does not stand for the precise time delay after which the function is executed. It stands for the minimum wait time after which at some point in time the function will be executed. 

<br>

> Take a look at the below code:

```javascript

function goCorona() {
   console.log('Stay Home, Stay Safe');
}

setTimeout(goCorona, 5000);

```

> That doesn’t mean that `goCorona` will be executed in 5s but rather that, in 5000 ms, `goCorona` will be added to the queue. The queue, however, might have other events that have been added earlier — the function `goCorona` will have to wait. The idea here is the above code gaurantees that `Stay Home, Stay Safe` will be printed anytime after `5000ms`.

<br>

- **`setTimeout` returns `timeoutID`** - The returned `timeoutID` is a positive integer value which identifies the timer created by the call to `setTimeout()`. This value can be passed to `clearTimeout()` to cancel the timeout.

- **The Event Loop has one simple job — to watch the Call Stack and the Callback Queue**. If the Call Stack is empty, it will take the first event from the queue and will push it to the Call Stack, which effectively runs it.

<br>

## About Me


```js

// About me

import { Speaker } from 'HackOn';

let user =  {
      Name: 'Vinit Shahdeo',
      Company: 'Postman',
      Profile: 'Software Engineer',  // Ex VITian
      Twitter: '@Vinit_Shahdeo'
    },
    title: 'Event loop in JavaScript and rise of Asynchronous behaviour';

_.assign(new Speaker(), user, new Event(title));

```

<br>

|                                                                                         <a href="https://fayz.in/stories/s/1522/0/?ckt_id=ZGL1ZGVk&title=story_of_vinit_shahdeo"><img src="https://raw.githubusercontent.com/vinitshahdeo/Water-Monitoring-System/master/assets/vinit-shahdeo.jpg" width=150px height=150px /></a>                                                                                         |
| :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|                                                                                                                                        **[Vinit Shahdeo](https://www.linkedin.com/in/vinitshahdeo/)**                                                                                                                                        |
| <a href="https://twitter.com/Vinit_Shahdeo"><img src="https://raw.githubusercontent.com/vinitshahdeo/Water-Monitoring-System/master/assets/twitter.png" width="32px" height="32px"></a> <a href="https://www.facebook.com/vinit.shahdeo"><img src="https://raw.githubusercontent.com/vinitshahdeo/Water-Monitoring-System/master/assets/facebook.png" width="32px" height="32px"></a> <a href="https://www.linkedin.com/in/vinitshahdeo/"><img src="https://raw.githubusercontent.com/vinitshahdeo/Water-Monitoring-System/master/assets/linkedin.png" width="32px" height="32px"></a> |

[![GitHub followers](https://img.shields.io/github/followers/vinitshahdeo.svg?label=Follow%20@vinitshahdeo&style=social)](https://github.com/vinitshahdeo/) 

[![Twitter Follow](https://img.shields.io/twitter/follow/Vinit_Shahdeo?style=social)](https://twitter.com/Vinit_Shahdeo)

> **Learn more about me [here](https://fayz.in/stories/s/1522/0/?ckt_id=ZGL1ZGVk).**

#### Well, in this unprecedented time, you all have showed interest. I thank all of you for joining me. :hugs: Stay Safe at home.

:mask: :house:
<br><br>

```javascript
/**
 * 
 * Let's fight for Corona together!
 */
function stayAtHome() {
  eat();
  sleep();
  code();
  repeat();
}

while(_.isAlive(new Virus('COVID-19'))) {
  // Stay home, Stay safe
  stayAtHome();
}
```
<br>

## :confused: Any doubts? 

> :point_right: You can find the [PPT](https://github.com/vinitshahdeo/Event-Loop-In-JavaScript/blob/master/doc/%5BHack0N%5D%20Event%20loop%20in%20JS%20-%20PDF%20(5).pdf) inside `docs` folder.

### :link: [Click here](https://github.com/vinitshahdeo/Event-Loop-In-JavaScript/raw/master/doc/%5BHack0N%5D%20Event%20loop%20in%20JS%20-%20PDF%20(5).pdf) to download the PPT.

### :fountain_pen: Feel free to shoot your doubts [here](https://github.com/vinitshahdeo/Event-Loop-In-JavaScript/issues/1).

```javascript

  ___      _     ___  ___                  
 / _ \    | |    |  \/  |                  
/ /_\ \___| | __ | .  . | ___              
|  _  / __| |/ / | |\/| |/ _ \             
| | | \__ \   <  | |  | |  __/             
\_| |_/___/_|\_\ \_|  |_/\___|             
                                           
                                           
  ___              _   _     _             
 / _ \            | | | |   (_)            
/ /_\ \_ __  _   _| |_| |__  _ _ __   __ _ 
|  _  | '_ \| | | | __| '_ \| | '_ \ / _` |
| | | | | | | |_| | |_| | | | | | | | (_| |
\_| |_/_| |_|\__, |\__|_| |_|_|_| |_|\__, |
              __/ |                   __/ |
             |___/                   |___/ 

```

<br>

## :bowtie: Checkout my recent works below:

> [![GitHub stars - COVID-19 Vinit Shahdeo](https://img.shields.io/github/stars/vinitshahdeo/COVID19?label=LEAVE%20A%20Star%20on%20GitHub&logo=github&style=for-the-badge)](https://github.com/vinitshahdeo/COVID19/)

- ### [Live Updates of Reported Corona Cases](http://corona-cases-india.netlify.com/) :mask:
- ### [COVID-19 Tracker :bar_chart: | INDIA :india:](https://indiafightscorona.netlify.app/)
- ### Consider leaving a star :star: [here](https://github.com/vinitshahdeo/COVID19).<sup>To be open-sourced pretty soon.</strong></sup>

<br>

---

```javascript
// thank you :)

const THANK_YOU_MSG = `Thank you so much for being here! 
	you were an amazing audience`;

let sayThanks = (viewer) => { return THANK_YOU_MSG };

_.forEach(allViewers, function (viewer) {
	_.times(Number.MAX_SAFE_INTEGER, sayThanks(viewer));
});

```
---

[![Thank you for watching this](./assets/thank-you.gif)](https://youtu.be/zsRv8g3C4rY?t=215)

[![Twitter Follow](https://img.shields.io/twitter/follow/Vinit_Shahdeo?style=social)](https://twitter.com/Vinit_Shahdeo)
 [![GitHub followers](https://img.shields.io/github/followers/vinitshahdeo.svg?label=Follow%20@vinitshahdeo&style=social)](https://github.com/vinitshahdeo/) 


