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
        <p class='text1'>
            以前Vue.jsで作ったアプリをより良いものにしたいと思って、制作を計画しました。<br>
            以前のものは、「リロードしたら消えていく」「チェックボックスをクリックす<br>
            ると消える仕組みだが、気になる部分があった」「チェックボックスだと単純す<br>
            ぎる」と感じ、これらを改善するように努めた。<br>
            まず、リロードしたら消える点に関しては、Vuex・Vuex PersistedStateを利用<br>
            して解決しました。チェックボックスの部分は、完了したことを明示する方<br>
            法として、表示を切り替える方法を採用しました。
        </p>

        <p class='text2'>
            以前Vue.jsで作ったアプリをより良いものにしたいと思って、制作を計画しました。以前のものは、「リロードしたら消えていく」「チェックボックスをクリックすると消える仕組みだが、気になる部分があった」「チェックボックスだと単純すぎる」と感じ、これらを改善するように努めた。まず、リロードしたら消える点に関しては、Vuex・Vuex PersistedStateを利用して解決しました。チェックボックスの部分は、完了したことを明示する方法として、表示を切り替える方法を採用しました。
        </p>
        <h4>使用言語・技術等</h4>
        <p>JavaScript・Vue.js・Vuex・Vuex PersistedState・No Class CSS・Netlify</p>
    </div>
</template>