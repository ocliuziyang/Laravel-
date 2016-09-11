#Laravely使用Ajax删除数据(使用_method进入隐式路由)

>1.说明

```php
use Illuminate\Http\Request;
use App\Task;
use Log;

Route::get('/tasks', function(){

    $tasks = Task::where('id', '>' , '0')->get();

    return view('tasks', compact('tasks'));

});

Route::post('/tasks', function(Request $request){

    $name = $request->name;
    Task::create(
        ['name'=> $name]
    );
    return redirect(url('/tasks'));
});

Route::delete('/task', function (){

    Log::info('进入删除方法');
    dd(1);

});
```