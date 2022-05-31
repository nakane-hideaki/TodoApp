# WebページのURL(ルーティング)について

Laravelでは、どのURLにアクセスされたら、どの処理を呼び出すのかというリストが作成されている。  

そのリストは、`backend/web/admin/routes/web.php`にある。  

（ルーティングの例）
```
Route::name('bootstrap.index')->get( 'bootstrap/index', function () { 
    return view('front.home.bootstrap.index'); 
});
```

このようなルーティングがあるとき、get()の中身が重要になる。get()の中の、1つ目のシングルクォーテーションの中の文字が、`localhost/`以降のURLの文字列になる。その後に return view() と書いてある場合、その中の()の中の文字は、`backend/web/admin/resources/views/`の中のフォルダ名、ファイル名を表している。  

<br>

例）  
`return view('front.home.bootstrap.index');`  
  
とある場合、`backend/web/admin/resources/views/front/home/bootstrap/index.blade.php`が表示される。  
  
