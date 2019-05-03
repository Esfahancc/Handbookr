# Install
```
curl -sL https://rpm.nodesource.com/setup_10.x | sudo bash -
yum install -y nodejs libpng-devel
```

## Obfuscator
```
npm install -g javascript-obfuscator

javascript-obfuscator ./resources/js --compact true --control-flow-flattening true --control-flow-flattening-threshold 1 --dead-code-injection true --dead-code-injection-threshold 1 --debug-protection true --debug-protection-interval true --disable-console-output true --identifier-names-generator 'mangled' --log false --rename-globals false --rotate-string-array true --self-defending false --string-array true --string-array-encoding 'rc4' --string-array-threshold 1 --transform-object-keys true --unicode-escape-sequence false --domain-lock 'www.test.com'
```