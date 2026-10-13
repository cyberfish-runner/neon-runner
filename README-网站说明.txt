霓虹跑者 NEON RUNNER · 官网说明（Netlify + GitHub Releases 版）
=====================================================================
上线域名（免费）: https://cyberfish-runner.netlify.app
游戏本体哈希    : EB369157067CAC72FD27918F78CCD02F012E3941971762D8C22AAABA62240368

【文件清单】
  index.html            官网首页（单页；HTML + 内联 CSS；无 JS、无框架、无外部依赖）
  play.html             游戏本体（在线试玩用；与桌面版 app/index.html 是同一份文件）
  netlify.toml          Netlify 部署配置（图片长期缓存 + 安全响应头；无需构建）
  robots.txt            搜索引擎抓取规则（含 sitemap 地址）
  sitemap.xml           站点地图（首页 + play.html）
  README.md             给 GitHub 仓库首页看的项目说明
  README-网站说明.txt    本文件
  images/icon.png       网站图标 / 应用图标（256×256）
  images/og-cover.png   社交分享封面（1200×630）
  images/shot-1.png     游戏截图 LV.01 数据贫民窟
  images/shot-2.png     游戏截图 LV.02 霓虹城区（首页大图）
  images/shot-3.png     游戏截图 LV.02 横移平台跨坑
  images/shot-4.png     游戏截图 LV.03 企业高塔（三连激光阵）
  images/shot-5.png     游戏截图 LV.01 深坑与全息平台
  合计约 2.4 MB，整个文件夹可直接部署

---------------------------------------------------------------------
【部署到 Netlify】（两种方式任选）

方式 A：拖拽部署（最快，60 秒上线，不需要 git）
  1. 打开 https://app.netlify.com/drop
  2. 把整个「网站发布」文件夹拖进网页
  3. 等十几秒，Netlify 会给你一个随机域名，例如 https://silly-cat-123.netlify.app
  4. 改名字：Site configuration → Site details → Change site name → 填 cyberfish
     改完地址就是 https://cyberfish-runner.netlify.app
     （如果 cyberfish 被占用，换个名字，然后把 index.html 里的域名一起改掉）

方式 B：连接 GitHub 仓库（推荐长期用，改了自动重新部署）
  1. 先在 GitHub 建仓库并把本站文件传上去（见下一节）
  2. Netlify → Add new site → Import an existing project → GitHub → 选仓库
  3. Build command 留空，Publish directory 填 .   （netlify.toml 里已经写好）
  4. Deploy site，之后每次 push 都会自动重新部署

---------------------------------------------------------------------
【GitHub 仓库 + Releases 放安装包】（全程网页操作，不需要装 git）

  一、建仓库
    1. 打开 https://github.com/new
    2. Repository name 填  neon-runner
    3. 选 Public（必须公开，否则别人下载不了 Release 附件）
    4. 不要勾 Add a README（我们要自己传）
    5. Create repository

  二、把网站文件传上去
    在空仓库页面点「uploading an existing file」，
    把「网站发布」文件夹【里面的所有文件】拖进浏览器
    （index.html、play.html、netlify.toml、robots.txt、sitemap.xml、
      README.md、README-网站说明.txt、images 文件夹）
    然后 Commit changes。

  三、建 Release 并上传两个安装包
    1. 进仓库 → 右侧 Releases → Create a new release
    2. Choose a tag 填  v1.0.0  → 点 Create new tag
    3. Release title 填  霓虹跑者 v1.0.0
    4. 描述里可以贴下面这段（含 SHA256 校验值）
    5. 把两个 exe 拖进「Attach binaries」区域：
         D:\NeonRunner\dist\NeonRunner-1.0.0-setup.exe
         D:\NeonRunner\dist\NeonRunner-1.0.0-portable.exe
       （每个约 106 MB，上传要几分钟）
    6. Publish release

    上传完成后，两个文件的下载直链是：
      https://github.com/<你的用户名>/neon-runner/releases/download/v1.0.0/NeonRunner-1.0.0-setup.exe
      https://github.com/<你的用户名>/neon-runner/releases/download/v1.0.0/NeonRunner-1.0.0-portable.exe

  四、把用户名填回网站
    在 index.html 里搜索： cyberfish-runner
    会命中 2 处（安装版 / 便携版的两个 href），替换成你的 GitHub 用户名即可。
    建议用编辑器的「全部替换」一次搞定。

---------------------------------------------------------------------
【Release 描述可以贴这段】

  ## 霓虹跑者 NEON RUNNER v1.0.0

  赛博朋克 2D 横版平台跳跃 · 三关完整流程 · 99 枚芯片

  | 文件 | 说明 | 大小 |
  |---|---|---|
  | NeonRunner-1.0.0-setup.exe | 安装版（推荐）：建桌面与开始菜单快捷方式，可正常卸载 | 约 106 MB |
  | NeonRunner-1.0.0-portable.exe | 便携版：免安装，双击即玩 | 约 106 MB |

  **系统要求**：Windows 10（1809 及以上）/ Windows 11，64 位。无需联网、无需安装任何运行库。

  **安装时若提示「Windows 已保护你的电脑」**：这是 SmartScreen 对未签名程序的默认拦截，不是病毒。
  点「更多信息」→「仍要运行」即可。

  **SHA256 校验**
  ```
  NeonRunner-1.0.0-setup.exe
  7093CD2A351D2812AC808D8BD8E4FD94F3E85AD5DF7DFEF7F421B05EBEB1986F
  NeonRunner-1.0.0-portable.exe
  031C1D9DEF6A5E0DFEBDA24C224CC90064AC47AE50510A01AF017D20419D21FA
  ```

  官网与在线试玩：https://cyberfish-runner.netlify.app/

---------------------------------------------------------------------
【上线自检清单】
  □ 访问 https://cyberfish-runner.netlify.app/            → 出现官网首页
  □ 点「在线开始玩」                                → 进 play.html 能玩（标题页显示「存档 : localStorage 已挂载」）
  □ 点「下载 Windows 安装版」                        → 真的开始下载（不是 404）
  □ 点「下载免安装便携版」                           → 真的开始下载
  □ 手机打开                                        → 单列布局，不横向滚动
  □ 把网址发到微信/QQ                                → 分享卡片显示标题与封面
  □ 打开 https://cyberfish-runner.netlify.app/robots.txt    → 能看到内容
  □ 打开 https://cyberfish-runner.netlify.app/sitemap.xml   → 是合法 XML

---------------------------------------------------------------------
【注意：GitHub 下载在国内可能偏慢】
  GitHub Releases 的下载走 objects.githubusercontent.com，中国大陆访问经常很慢甚至超时。
  如果发现访客反馈下载困难，可以二选一：
    A) 再传一份到国内网盘（蓝奏云、阿里云盘、夸克），在页面上加一个「国内备用下载」按钮
    B) 买一台国内对象存储（阿里云 OSS / 腾讯云 COS），把 exe 放上去，换成直链
  要加备用下载按钮的话，把链接给我，我帮你改页面。

---------------------------------------------------------------------
【以后想换自己的域名】
  1. 买个域名（阿里云/腾讯云/Namecheap 都行，.com 约 ¥60/年）
  2. Netlify → Domain management → Add a domain → 填你的域名
  3. 按提示到域名商那里把 DNS 指过去（Netlify 会给你 2 条记录）
  4. 等 DNS 生效（几分钟到几小时），Netlify 会自动签发 HTTPS 证书
  5. 换完后在 index.html 里搜索 cyberfish-runner.netlify.app，全部替换成新域名
     （canonical / og:url / og:image / twitter:image / JSON-LD / robots.txt / sitemap.xml）
     建议保留 cyberfish-runner.netlify.app 也能访问（Netlify 会自动做跳转）
