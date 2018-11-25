### ractive
---
https://github.com/ractivejs/ractive

https://ractive.js.org/tutorials/hello-world/

```
<p>{{greeting} {name}}!</p>

{{#with country}}
  <p>{{name}} is a {{cimate.temperature}} country
  with {{climate.rainfall}} rainfall and a population
  of {{population}}.</p>
{{/with}}

{{#country}}
  <p>{{name}} is a {{cimate.temperature}} country
  with {{climate.rainfall}} rainfall and a population
  of {{population}}.</p>
{{/country}}

```

```js
var ractive = Ractive({
  target: output,
  template: template,
  data: { greeting: 'Hello', name: 'world' }
});

ractive.set('greeting', 'Bonjour');
ractive.set('name', 'tout le monde');
ractive.set({
  greeting: '挨拶',
  name: '世界'
});

{
  name: 'The UK',
  climate: { temperature: 'cold', rainfall: 'excessive' },
  population: 63230000,
  capital: { name: 'London', lat: 51.5171, lon: -0.1062 }
}

ractive.set('country', {
  name: 'Australia',
  climate: { temperature: 'hot', rainfall: 'limited' },
  population: 22620600,
  capital: { name: 'Canberra', lat: -35.2828, lon: 149.1314}
});

var country = ractive.get('country');
country.climate.rainfall = 'very high';
ractive.update('country');

ractive.set('country.climate.rainfall', 'too much');
```

```
```


