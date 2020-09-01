<template>
    <div>
        <div class='detail'>
            <h3>ToDo Manager</h3>
            <button class='btn'>
                <a class='goToApp' href='https://vuetodoappagain.netlify.app'
                    target='_blank' rel='noopener noreferrer'>
                Go to App <i class='fas fa-caret-square-right'></i>
                </a>
            </button>
            <a class='githubIcon2' href='https://github.com/azufb/VueToDoAgain' target='_blank' rel='noopener noreferrer'><i class='fab fa-github fa-2x'></i></a>
        </div>
        <h4>制作のきっかけ</h4>
        <p>
            以前Vue.jsで作ったアプリをより良いものにしたいと思って、制作を計画。<br>
            今回は、CDN版ではなく、Vue CLIを利用。<br>
            以前のものは、「リロードしたら消えてしまう」「チェックボックスをクリック<br>
            すると消える仕組みだが、不具合があった」「チェックボックスだとあまりにも<br>
            単純すぎる」と感じ、これらを改善するように努めた。<br>
            まず、リロードしたら消える点に関しては、Vuex・Vuex PersistedStateを<br>
            利用することで、解決。チェックボックス の部分は、「完了した」ことを明示<br>
            できる方法として、表示を切り替える方法を採用した。(スマホ非推奨)
        </p>
        <h4>使用言語・技術等</h4>
        <p>JavaScript・Vue.js・Vuex・Vuex PersistedState・No Class CSS・Netlify</p>
    </div>
</template>