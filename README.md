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

## 🥇 [项目 A: EnterpriseFlow 流程协作平台]

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

## 🥇 [项目 B: zp-element-plus Vue 3 组件库]

## 技术栈
Vue 3 | Vite | TypeScript | VitePress | async-validator | Vitest | FontAwesome | @floating-ui/vue | @popperjs/core | lodash-es

## 项目描述
这是一个企业级 Vue 3 UI 组件库项目，提供 11+ 个高质量组件和完整的文档系统。项目采用现代化的前端技术栈，实现了完整的组件开发、文档生成、表单验证、类型定义等核心功能。组件库支持 TypeScript，提供完善的类型提示和类型检查，帮助开发者快速构建高质量的企业级应用。采用 VitePress 构建文档站点，支持在线预览和代码展示，提供优秀的开发体验。

## 我的职责

### 组件库架构设计
主导设计了组件库的整体架构，采用模块化的组件设计模式，每个组件独立封装，包含组件文件、类型定义、样式文件和测试文件。实现了统一的组件命名规范（zp-前缀），确保组件库的一致性和可维护性。设计了组件 Props、Emits、Slots 的完整类型定义体系，提供良好的 TypeScript 支持。

### 核心组件开发
开发了 11+ 个高质量组件，覆盖表单、数据展示、反馈、导航等业务场景：

**表单类组件：**
- **Form & FormItem**：实现了完整的表单验证系统，基于 async-validator 实现异步验证，支持自定义验证规则、验证触发时机（input/blur/change）、验证状态管理（init/success/error/loading）。通过 provide/inject 实现了 Form 和 FormItem 的通信机制，支持表单级别的 validate、resetFields、clearValidate 方法。

- **Input**：实现了功能丰富的输入框组件，支持清空、密码显示切换、图标插槽、尺寸控制、只读状态等。封装了防抖机制优化验证错误打印，避免频繁的控制台输出。实现了与 FormItem 的深度集成，自动触发验证。

- **Select**：实现了功能强大的选择器组件，支持基础选择、可清空、禁用状态、可搜索、远程搜索、自定义选项渲染、自定义过滤方法等功能。使用 Tooltip 组件实现下拉菜单，支持键盘导航和鼠标交互。

- **Switch**：实现了开关组件，支持布尔值、字符串、数字等多种值类型，支持文字描述、禁用状态、多种尺寸等配置。

**数据展示类组件：**
- **Collapse & CollapseItem**：实现了折叠面板组件，支持手风琴模式、禁用状态、自定义标题和内容插槽。

- **Dropdown & DropdownMenu & DropdownItem**：实现了下拉菜单组件，支持菜单项点击、隐藏时机控制、自定义触发方式。

**反馈类组件：**
- **Alert**：实现了警告提示组件，支持多种类型（success/warning/info/danger）和可关闭功能。

- **Message**：实现了消息提示组件，支持多种类型、可关闭、朴素样式、自定义持续时间。使用 createMessage 方法实现全局调用，支持消息队列管理和位置控制。

- **Tooltip**：实现了文字提示组件，基于 @floating-ui/vue 实现智能定位，支持多种触发方式（hover/click/focus）和位置控制。

**基础组件：**
- **Button**：实现了按钮组件，支持多种类型、尺寸、状态（loading/disabled）、样式（plain/round/circle/text）和图标。

- **Icon**：基于 FontAwesome 实现了图标组件，支持图标库的统一管理和使用。

### 表单验证系统
实现了完整的表单验证体系，基于 async-validator 封装了验证逻辑。支持多种验证规则（required、type、min、max、len、pattern、validator），支持自定义验证函数实现复杂验证逻辑。实现了验证状态的响应式管理，包括验证状态（init/success/error）、错误消息、加载状态。通过 validateState 实现了验证状态的统一管理，支持 clearValidate 清除验证状态，resetField 重置字段值和验证状态。

### 文档系统开发
基于 VitePress 构建了完整的文档系统，实现了以下功能：

**自动侧边栏生成**：通过 `getComponentsSidebar` 函数自动扫描组件目录，动态生成侧边栏配置，支持新增组件自动出现在文档中，无需手动配置。

**Demo 展示系统**：实现了 DemoBlock 组件，支持代码和演示效果的分离展示。通过 markdown-it-container 插件实现了 `::: demo` 语法，支持在文档中直接编写 Vue 组件代码并实时预览。解决了组件注册问题，在 VitePress 主题中全局注册所有组件，确保 Demo 中可以使用所有组件。

**文档编写规范**：为每个组件编写了完整的使用示例和 API 文档，包括基础用法、各种配置选项、事件说明、插槽说明等。所有示例都支持在线预览，用户可以直观看到组件效果。

### 组件注册与主题系统
在 VitePress 主题中实现了组件的全局注册系统，通过 `enhanceApp` 方法注册所有组件，确保文档中的 Demo 可以正常使用。解决了 VitePress 2.0.0-alpha.15 版本的兼容性问题，通过配置优化解决了 VPTeamPageTitle.vue 的错误。实现了样式文件的统一导入，确保组件样式在文档中正确显示。

### 工具函数封装
封装了多个可复用的工具函数和组合式函数：

**组合式函数（Composables）：**
- **useClickOutside**：实现了点击外部区域检测，用于下拉菜单、弹出框等组件的关闭逻辑。

- **useEventListener**：封装了事件监听器的添加和移除，确保组件卸载时正确清理事件监听。

- **useZindex**：实现了 Z-index 的自动管理，确保弹出层按照正确的层级显示。

**工具函数：**
- **RenderVnode**：实现了 VNode 的渲染工具，用于 Select 组件的自定义选项渲染。

### 类型系统设计
为所有组件设计了完整的 TypeScript 类型定义，包括：
- **Props 接口**：定义组件的所有属性及其类型
- **Emits 接口**：定义组件的事件及其参数类型
- **Instance 接口**：定义组件暴露的方法和属性
- **Context 接口**：定义组件间通信的上下文类型

通过完整的类型定义，提供了良好的开发体验和类型安全保障。

### 样式系统设计
设计了统一的样式系统，包括：
- **CSS 变量**：定义了主题颜色、尺寸等变量，支持主题定制
- **重置样式**：提供了 CSS 重置，确保跨浏览器一致性
- **组件样式**：每个组件都有独立的样式文件，使用 Scoped CSS 避免样式冲突
- **响应式设计**：所有组件都支持响应式布局

### 测试体系搭建
基于 Vitest 搭建了单元测试体系，为关键组件编写了测试用例。使用 @vue/test-utils 进行组件测试，确保组件的功能和交互正确性。

### 开发工具链配置
配置了完整的开发工具链：
- **ESLint**：配置了 Vue 3 和 TypeScript 的代码检查规则
- **Prettier**：配置了代码格式化规则
- **TypeScript**：配置了严格的类型检查
- **Vite**：配置了开发服务器和构建优化
- **Vitest**：配置了测试环境和覆盖率报告

### 项目文档完善
编写了完整的项目文档，包括：
- **README.md**：详细的项目说明、快速开始、使用示例等
- **组件文档**：每个组件的使用文档和 API 文档
- **开发指南**：安装指南、开发规范、贡献指南等

### 问题解决与技术优化
解决了多个技术难点：
- **验证错误打印优化**：实现了防抖机制和错误消息去重，避免频繁的控制台输出
- **组件样式穿透**：使用 `:deep()` 实现了 FormItem 对 Input 组件样式的控制
- **错误消息显示**：解决了错误消息定位问题，确保错误信息正确显示在输入框下方
- **VitePress 兼容性**：解决了 VitePress 2.0.0-alpha.15 版本的已知问题
- **组件注册时机**：解决了组件在文档中的注册时机问题，确保 Demo 正常显示

### 代码质量保障
实现了严格的代码质量保障措施：
- **类型检查**：所有代码都通过 TypeScript 类型检查
- **代码规范**：遵循 Vue 3 Composition API 最佳实践
- **代码格式化**：使用 Prettier 统一代码格式
- **代码检查**：使用 ESLint 进行代码质量检查
- **测试覆盖**：关键功能都有测试用例覆盖

---

**项目成果**：成功构建了一个功能完善、文档齐全、类型安全的企业级 Vue 3 组件库，为团队提供了高质量的 UI 组件和优秀的开发体验。


* ** | [🔗 仓库源码](https://github.com/heidiug/element-zp-plus)]**

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
