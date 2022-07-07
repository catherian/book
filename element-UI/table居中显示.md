核心代码 :cell-style="rowStyle"  和 header-align="center"（控制表头居中显示）
```
<el-table :cell-style="rowStyle" :data="table_content">
            <el-table-column header-align="center" :label="val" v-for="(val, i) in table_head" :key="i">
                <template slot-scope="scope">{{table_content[scope.$index][i]}}</template>
            </el-table-column>
        </el-table>
```
同时，以上代码也是table的动态表格。对应的变量格式
```
            // 表头数据
            table_head: ["ID", "项目名", "报警时间", "总数"],
            // 表格内容数据
            table_content: [
                ["24", "20", "18", "2"],
                ["22", "20", "18", "2"],
                ["22", "20", "18", "2"],
                ["51", "21", "20", "6"],
                ["21", "20", "18", "2"],
            ],
```