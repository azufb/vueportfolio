<template>
    <div>
        <div class='detail'>
            <h3>ToDo Manager</h3>
            <button class='btn'>
                <a class='goToApp' href='https://todokanri.netlify.app'
                    target='_blank' rel='noopener noreferrer'>
                Go to App <i class='fas fa-caret-square-right'></i>
                </a>
            </button>
            <a class='githubIcon2' href='https://github.com/azufb/ToDoAppwithPraise' target='_blank' rel='noopener noreferrer'><i class='fab fa-github fa-2x'></i></a>
        </div>
        <h4>制作のきっかけ</h4>
        <img src='../../todokanri.png'>
        <p class='text1'>
            前回、ToDoアプリを作った時に、「チェックボックスにチェックしただけでは、<br>
            タスクの完了・未完了が分かりづらい」というご意見を頂きました。<br>
            そこで、今回は、この課題を改善したアプリにしようと考え、制作しました。<br>
            In ProgressエリアとDoneエリアで表示が分かれており、In Progressエリアで表<br>
            示されるDONEボタンを押すと、Doneエリアにタスクが移動することで、完了<br>
            ・未完了を一目で確認できるようにしました。
        </p>

        <p class='text2'>
            以前Vue.jsで作ったアプリをより良いものにしたいと思って、制作を計画しました。以前のものは、「リロードしたら消えていく」「チェックボックスをクリックすると消える仕組みでしたが、気になる部分があった」「チェックボックスだと単純すぎる」と感じ、これらを改善するように努めました。まず、リロードしたら消える点に関しては、Vuex・Vuex PersistedStateを利用して解決しました。チェックボックスの部分は、完了したことを明示する方法として、表示を切り替える方法を採用しました。
        </p>
        <h4>使用言語・技術等</h4>
        <p>JavaScript・Vue.js・Vuex・Vuex PersistedState・Netlify</p>
    </div>
</template>