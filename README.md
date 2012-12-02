# jQuery.paint

## 概要
Webサイトに簡単にお絵かき機能を実装できるよ  
* 本当に必要最低限なお絵かき機能のみ
* やり直し(Undo)は１回のみ可

## デモページ
http://hotolab.net/jquery.paint/

## オプション
* width  
キャンバスの横幅。
* height  
キャンバスの縦幅。
* file  
読み込む画像のパス。  
このオプションを指定したときはwidthとheightオプションは無視され、画像のサイズがキャンバスのサイズになる。
* upload  
保存時に呼び出される関数。  
ひとつ目の引数に画像のデータがBase64形式で渡されるので、あとは各自Ajaxでサーバーサイドに送るなり煮るなり焼くなり。  

他にもオプションあるけどあんまり使わなさそうなのでソースコード見てください（ぇ

## つかいかた例
    $('#oekaki').paint({
    	file : '/image/photo.jpg',
    	upload : function(image){
    		$.post('/upload.php', { data: image });
    	}
    }); 


