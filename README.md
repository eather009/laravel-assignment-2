# Steps for Assignment tasks

## 1. Controller Create
<code>php artisan make:controller ProfileController</code>

## 2. Controller Index function
<code>
class ProfileController extends Controller
{<br/>
public function index(Request $request, $id)
{<br/>
        $name = "Donal Trump";<br/>
        $age = "75";<br/>
        $data = array(<br/>
            "id" => $id,<br/>
            "name" => $name,<br/>
            "age" => $age,<br/>
        );<br/>
        $name = "access_token";<br/>
        $value = "123-XYZ";<br/>
        $minutes = 1;<br/>
        $path = "/";<br/>
        $domain = $_SERVER['SERVER_NAME'];<br/>
        $secure = false;<br/>
        $httpOnly = true;<br/><br/>
        return response($data)->cookie($name,$value,$minutes,$path,$domain,$secure,$httpOnly);
    <br/>}
<br/>}
</code>


## 3. Route added
routes/web.php<br/><code>Route::get('/profile/{id}',[ProfileController::class,'index']);</code>

## 4. Create Server and Test by URL
<code>php artisan serve</code>

URL: http://127.0.0.1:8000/profile/1
