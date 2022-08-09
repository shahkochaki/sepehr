# sepehr
Sepehr System reservation system Laravel package
```bash
# Install Composer
curl -sS https://getcomposer.org/installer | php
```

Next, run the Composer command to install the latest stable version:

```bash
composer.phar require shahkochaki/sepehr
```

After installing, you can now use it in your code:

```php
   $ami = new \sepehr\api();
   if ($ami->connect('localhost:5038', 'myuser', 'mysecret', 'off') === false) {
      throw new \RuntimeException('Could not connect to Asterisk Management Interface.');
   }
   
   // // if you have a looping of command function
   // // set allowTimeout flag to true
   // $ami->allowTimeout();

   // $result contains the output from the command
   $result = $ami->command('core show channels');
   
   $ami->disconnect();
```
