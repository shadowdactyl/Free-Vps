# Free-Vps

$user = App\Models\User::findOrFail(1);


$user->password = Illuminate\Support\Facades\Hash::make('admin1234');
