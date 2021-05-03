<ul>
    <li>Clone your project </li><br>
    <li> Go to the folder application using <strong>cd</strong> command on your cmd or terminal
</li><br>
    <li> Run <mark>composer install</mark> on your cmd or terminal
</li><br>
    <li>Copy <mark>.env.example</mark>  file to <mark>.env</mark> on the root folder. You can type <mark>copy .env.example .env</mark> if using command prompt Windows or cp .env.example .env if using terminal, Ubuntu </li><br>
    <li> Open your .env file and change the database name (DB_DATABASE) to whatever you have, username (DB_USERNAME) and password (DB_PASSWORD) field correspond to your configuration.</li><br>
    <li> By default, the username is root and you can leave the password field empty. (This is for Xampp)</li><br>
    <li> By default, the username is root and password is also root. (This is for Lamp)</li><br>
    <li>Run <mark>php artisan key:generate</mark> </li><br>
    <li> Run <mark>php artisan migrate</mark>
</li><br>
    <li> Run <mark>php artisan serve</mark>
</li><br>
    <li> Go to <mark>localhost:8000</mark>
</li><br>
</ul>
