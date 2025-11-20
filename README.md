## 👋 你好，我是 [周平/heidiug]

我是一名来自 **成都信息工程大学** 的大四在读生，主攻前端开发方向。

我对使用代码构建流畅、美观且实用的 Web 界面充满热情。作为 **“异步实验室”** 的一员，我享受和一群热爱技术的伙伴们共同探索和解决难题。

在代码之外，我还是校羽毛球代表队的一员。竞技体育教会了我 **“在高压下保持专注”** 和 **“极致的团队协作”**——我相信这些品质在开发中同样重要。

---

### 💻 我的技术栈 (My Tech Stack)

我熟悉现代前端开发流程，并热衷于使用 Vue 3 和 TypeScript 构建项目。

| 类别 | 技术 |
| :--- | :--- |
| **前端核心** | `HTML` `CSS (Sass/Less)` `JavaScript (ES6+)` **`TypeScript`** |
| **框架与库** | **`Vue 3` (主力)** `Vue 2` `Vue-Router` `Pinia` |
| **后端与工程化** | `Node.js` `Vite` `Webpack` |
| **网络与工具** | `AJAX (Axios)` `RESTful API` `Git` |

---

#### 🥇 [项目 A: EnterpriseFlow 流程协作平台]

* **技术栈:** `Vue 3` `Vite` `TypeScript` `Pinia` `Element-Plus` `LogicFlow` `ECharts` `IndexedDB` `Axios`

* **项目描述:** 这是一个基于角色的（RBAC）中后台管理系统，提供流程设计、任务审批、数据看板、用户管理等核心功能。采用 Monorepo 架构，使用 pnpm workspace 管理多包项目，实现了完整的权限控制和动态路由系统。平台支持可视化流程设计、多级审批流程、实时数据统计等功能。

* **我的职责:**

    * **动态路由系统**：主导实现了基于权限的动态路由加载方案，通过 `router.addRoute()` 在路由守卫中根据用户权限动态添加路由，实现了菜单的权限控制。使用 `filterRoutesByPermission` 函数过滤路由，确保用户只能访问有权限的页面。解决了路由初始化时机问题，通过 `routesAdded` 标志位避免重复添加路由。

    * **按钮级权限控制**：封装了 `hasPermission` 和 `hasAnyPermission` 权限验证函数，支持单个权限和权限数组的检查。在路由的 `meta.permissions` 中定义权限要求，通过路由守卫和组件内权限检查实现细粒度的权限控制。支持 `admin` 角色的全权限访问，实现了灵活的权限体系。

    * **Token 认证与无感刷新**：使用 `axios` 拦截器封装了完整的认证体系。请求拦截器自动注入 `Bearer Token`，响应拦截器统一处理 401 错误，自动清除登录状态并跳转到登录页，支持重定向参数保持用户访问路径。解决了 Monorepo 架构中共享包不能直接依赖应用包的问题，通过依赖注入的方式在运行时注入 Pinia 和 Router 实例。

    * **业务组件封装**：封装了多个可复用的业务组件，提升了团队开发效率和代码复用率：
        - `NodePalette`：流程设计器的节点面板组件，支持拖拽创建节点
        - `PropertyPanel`：节点属性配置面板组件，支持动态表单配置
        - `ToolBar`：流程设计器工具栏组件，提供保存、撤销等操作
        - `UserForm`：用户信息表单组件，支持新增/编辑模式
        - `PermissionRequest`：权限申请表单组件，支持多选权限和审批流程
        - `MyTasks`：个人任务列表组件，支持状态筛选和详情查看

    * **可视化流程设计器**：基于 LogicFlow 实现了拖拽式流程设计器，支持节点创建、连线、属性配置、模板保存等功能。封装了 `useLogicFlow` composable 管理流程设计器的生命周期和状态，实现了节点类型管理、属性编辑、模板渲染等核心功能。

    * **数据可视化**：使用 ECharts 实现了多个数据看板组件，支持实时数据更新和交互式探索：
        - `ApprovalRateChart`：审批通过率趋势图，展示时间序列数据
        - `ProcessDurationPie`：流程耗时分布饼图，分析流程效率
        - `UserTaskHeatMap`：用户任务热力图，展示任务分布情况

    * **本地数据存储**：使用 IndexedDB 实现了本地数据库系统，封装了 `userTable`、`processTemplateTable`、`taskTable`、`approvalRecordTable` 等数据表，支持数据的增删改查操作。实现了数据的持久化存储，支持离线使用和快速数据访问。

    * **Monorepo 架构设计**：设计了多包项目结构，将通用工具函数抽取到 `flow-utils` 包中，包括权限验证、Token 管理、日期格式化、HTTP 请求封装等工具函数。通过依赖注入的方式解决了 Monorepo 中共享包不能直接依赖应用包的问题，实现了代码的复用和解耦。

* **[[🔗 稀土掘金](https://juejin.cn/post/7573170756868489268#heading-49] | [🔗 [仓库源码](https://github.com/heidiug/frontend-project.git)]**

#### 🥈 [项目 B: C端项目或个人作品]
* **技术栈:** `Vue 3` `Node.js` `...`
* **项目描述:** 一个仿 XXX 的 C 端应用 / 一个音乐播放器 / 一个...
* **我的职责:**
    * 实现了 XX 复杂交互（如无限滚动、拖拽...）
    * 使用 `Node.js` + `Koa/Express` 搭建了后端服务，提供了 `RESTful API`。
* **[🔗 在线访问] | [🔗 仓库源码]**

---

### 💡 团队与经历 (My Experience)

* **异步实验室 (Asynchronous Lab) | 核心成员** `(2022 - 至今)`
    * 在一个由技术驱动的社团中，参与过 X 次技术分享会（如 Vue 3 Composition API），并主导了 X 个团队项目的开发。
    * **收获:** 锻炼了快速学习新技术和团队协作编码的能力。

* **成都信息工程大学 | 校羽毛球代表队** `(2022 - 至今)`
    * 作为主力/替补队员，代表学校参加了 **“2024年四川省大学生羽毛球比赛”**。
    * **收获:** 强大的抗压能力、目标导向的执行力以及团队协作精神。

---

### 🎨 关于我 (A Little More About Me)

* 🏸 **竞技者:** 羽毛球是我的“第二专业”，我享受竞技带来的专注感。
* 🎨 **创造者:** 热爱绘画和设计，童年时获得过 **“成都市青少年人才艺术三等奖”**。这培养了我对 UI/UX 细节和美感的敏锐度。
* 🌱 **学习者:** 我目前正在深入学习 [例如：Vite 插件开发 / Three.js / 微前端]...

---

### 📫 如何联系我 (Find Me On)

* **Email:** `[1244252082@qq.com]`
* **掘金 (Juejin):** `[你的掘金主页链接]` (如果你有的话，强烈推荐)
* **Personal Blog:** `[你的博客链接]` (如果你有的话)

<p align="left">
  <img src="https://github-readme-stats.vercel.app/api?username=heidiug&show_icons=true&theme=tokyonight" alt="Your GitHub Stats" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=heidiug&layout=compact&theme=tokyonight" alt="Top Langs" />
</p>
