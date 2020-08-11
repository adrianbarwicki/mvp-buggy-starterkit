
# mvp-buggy-starterkit

Install npm packages:
```
cd mvp-buggy-lib-schematics
npm i
```

Then, run the schematics with
```
ng g mvp-buggy-lib-schematics:mvp-buggy-lib
```

After filling out the required params for the schematics (="name"), you will see the following error:
```
Cannot read property 'schematics' of undefined
```

Further debugging shows that the problems lie exactly here:
https://github.com/adrianbarwicki/mvp-buggy-lib-schematics/blob/master/mvp-buggy-lib-schematics/index.js#L16

which is `@nrwl/schematics`.
