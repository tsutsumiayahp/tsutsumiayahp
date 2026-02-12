https://github.com/tsutsumiayahp/tsutsumiayahp


基礎知識
html:ページの骨格と肉。配置する要素等はhtmlにて定義して組み立てる。
　→いじるとページの要素自体が変わる
css:ページの装飾、フォントの色や配置の間隔等、htmlで設定したものに対する細かいパラメータを設定するもの。
　→いじるとページの書式や表示等が変わる
javascript(JS):アニメーションやら外部変数の呼び出しやらいろいろできる便利なやつ
　→いじるとアニメーションやファイルを読み込んで表示しているものが変わる（既刊案内のコンテンツ等）

ファイル概要
assets/img
　→バナー等全ページ共有で使用する素材の格納場所（現在はPC版のアイコン画像を格納）
　　サイトのデザイン更新等が無い限りはいじらない

comics
　→既刊案内のページ、最低限のHTMLに既刊案内のグリッドを描写を呼び出している（js/script.js）
　　既刊案内を増やす際にはdata/comics.jsonへ新規の内容を追加→images/nowonsale/に画像を格納すれば更新される

css
　→サイトのデザイン更新等が無い限りはいじらない

data
　→仕事情報と既刊案内の一覧を管理するJSONファイルを格納、更新する場合は様式に合わせてJSONを更新すればそのまま反映される

images
　→サイトで使われている画像全般の格納場所
　　①直下で入っているものはトップページ用
　　②heroslider→ファーストビューのスライダー、
　　　更新する際は画像の追加とjs/script.jsの下記行を更新

　　　   const images = [
      "images/heroslider/hero1.png",
      "images/heroslider/hero2.png",
      "images/heroslider/hero3.png"
    ];

    const links = [
      "https://comic-walker.com/detail/KC_006257_S/episodes/KC_0062570000200011_E?episodeType=latest",
      "https://doax-venusvacation.jp/cartoon.html",
      "https://piccoma.com/web/product/8192/episodes"
    ];

　　③linestamp
　　　→トップのラインスタンプ用の画像メインhtmlの LINE STAMP GRID（3列1行）にハードコード

　　④nowonsale
　　　→既刊案内の素材
　　
　　⑤saishinkan
　　　→トップ最新刊用の素材htmlの TWO COLUMN (上段) <!-- LEFT COLUMN -->の下記部分が該当
        <div class="latest-cover">
          <a href="https://www.amazon.co.jp/dp/B0FV6LVRML/" target="_blank" rel="noopener noreferrer" class="latest-cover-link">
            <img src="images/saishinkan/SKnarr01_coverB1.png" alt="最新刊 表紙">
          </a>
        </div>
　　
　　⑥trial
　　　→試し読みの素材メインhtmlの TRIAL READING SECTIONにハードコード

js
　→Javascriptの格納先ファーストビューのバナー、↑に戻るボタンのアニメーション、PCSPのブレイクポイント調整、既刊案内の関数を制御

pages
　→プロトタイプの格納、新規ページを作る際のテストに表示できるようにパスを増設

works
　→仕事情報ページ、最低限のHTMLに既刊案内のグリッドを描写を呼び出している（js/script.js）
　　更新方法は概ねcomicsと同じ、書式を変える場合はcssをいじる