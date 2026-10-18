# Free-Vps

$user = App\Models\User::findOrFail(1);


$user->password = Illuminate\Support\Facades\Hash::make('admin1234');

curl -s http://127.0.0.1:8000/ | grep -Eo '(src|href)="[^"]+\.(js|css)[^"]*"'
