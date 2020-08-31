<template>
    <div id='cert'>
        <h2>保有資格</h2>
        <table>
            <thead>
                <tr>
                    <th>IT関連</th>
                    <th>取得年月</th>
                    <th>その他</th>
                    <th>取得年月</th>
                </tr>
            </thead>

            <tbody>
                <tr>
                    <td>ITパスポート試験</td>
                    <td>2020年06月</td>
                    <td>TOEIC 785点</td>
                    <td>2018年06月</td>
                </tr>

                <tr>
                    <td>Excel VBAスタンダード</td>
                    <td>2020年02月</td>
                    <td>日商ビジネス英語検定3級</td>
                    <td>2018年04月</td>
                </tr>

                <tr>
                    <td></td>
                    <td></td>
                    <td>ファイナンシャル・プランニング技能士3級</td>
                    <td>2018年03月</td>
                </tr>

                <tr>
                    <td></td>
                    <td></td>
                    <td>日商簿記3級</td>
                    <td>2017年02月</td>
                </tr>
            </tbody>
        </table>

        <Skills />
        
    </div>
</template>

<script>
import Skills from './Skills.vue';

export default {
    name: 'cert',
    components: {
        Skills,
    }
}
</script>