## What's a "configuration object"?

A configuration object is just a plain ol' JavaScript object that's used to configure something. For example:

```
var settings = {
   frosting: 'buttercream',
   colors: ['orange', 'blue'],
   layers: 2,
   isRound: true
};
```

...the settings configuration object can be used in the imaginary MakeCake constructor function:

`const myDeliciousCake = MakeCake( settings );`

Alternatively, the settings object could be passed in directly:

```
const myDeliciousCake = MakeCake({
   frosting: 'buttercream',
   colors: ['orange', 'blue'],
   layers: 2,
   isRound: true
});
```
