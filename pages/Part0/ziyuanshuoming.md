### 项目资源说明

<p>为统一、整合项目中的各类css、js、图片等资源，防止重复文件过多，引用不必要的文件等，现在整合项目中所用到的资源，请按照以下资源目录结构来进行存储。</p>

<pre>
<code>
--- assets                     静态资源文件库               
 | --- css               
    |--- main.css              框架全局样式文件
    |--- other.css             其他样式覆盖文件
 | ---- fonts                  阿里图标库
 | ---- img                    图片库
 | ---- jq                     jquery版本库
 | ---- js  
    |--- public.js             公用方法封装文件
 | ---- scss                   scss文件库
    |--- main.scss             框架样式scss文件
---- components                框架封装的各类功能组件
---- utils                     其他组件、工具库
</code>
</pre>

<p><strong>【重要】</strong>在此框架中，引入文件可以用绝对路径符号:<em>@</em>，路径为根目录下的src文件夹。比如引入一个css文件：<em>import '@/assets/css/a.css'</em></p>

- <em>src/assets/css/main.css</em>：框架主要样式文件，由 main.scss 自动生成，禁止修改、删除！！！
- <em>src/assets/fonts</em>：阿里图标库，具体使用说明请查看[阿里图标库](icon.md)
- <em>src/assets/css/other.css</em>：特殊样式文件，覆盖原有样式，需单独引入。
- <em>src/assets/jq</em>：存放所有的 jquery 文件，引入 jq 前请先查看此文件夹内是否已经存在。
- <em>src/assets/js/public.js</em>：公用方法的封装文件，比如搜索、弹窗等等。尽量减少同样功能的方法声明
- <em>src/assets/scss/main.scss</em>：框架样式来源文件，采用 scss 预处理方式，统一、规范化框架样式声明
- <em>src/components</em>：在开发中封装的各类功能组件，比如表格、附件上传、Tree 等等。
- <em>src/utils</em>：存放其他组件、工具，比如第三方上传附件工具等。
