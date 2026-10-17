# Free-Vps

echo "=== CODESPACE ==="
echo "$CODESPACE_NAME"

echo "=== VITE FILES ==="
ls -la public/hot public/build/manifest.json 2>&1

echo "=== APP URL ==="
grep '^APP_URL=' .env

echo "=== SERVER LOG ==="
tail -n 40 /tmp/matrix-panel-serve.log

echo "=== LOGIN RESPONSE ==="
curl -s -o /dev/null -w "HTTP %{http_code}\n" http://127.0.0.1:8000/login


App\Models\User::select('id', 'name', 'email', 'is_admin')->get();
