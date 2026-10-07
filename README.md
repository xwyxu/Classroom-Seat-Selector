# 智慧选座 —— 更快更强更便捷的班级智能化管理工具

今天我发布了「智慧选座」软件，它是更快更强更便捷的班级智能化管理工具。

选座位用的一套工具。全班 53 人，4 个大组，58 个座位。

**班主任把名单和顺序导进来之后，剩下的事系统自己完成：自动叫号，学生一个一个上台点座位，坐完自动换下一位。**

---

## 一、选座位是怎么进行的

老师把名单和顺序导进来之后就交给系统了。**剩下的事它自己完成：自动叫号，学生一个一个上台点座位，坐完自动换下一位。** 老师不用喊，也不用挨个点。

<img width="1432" height="914" alt="auto-assign" src="https://github.com/user-attachments/assets/fae1c5fc-0ea3-464a-8977-539df2278d78" />


主流程就是这一个圈：**叫号 → 上台 → 点座 → 自动换下一位**。志愿只是其中的一个可选分支。

### 叫号是自动的

老师把三个开关打开，系统就会用语音喊：

- **「请当前同学上台」** —— 喊到谁，屏幕上就是谁
- **「请下一位同学准备」** —— 下一位同时喊，不用临场找人

同学甲点完座位坐下，系统自动跳到同学乙并喊他上台。右边的「已完成选座」也在同步记录。

> 三个人都在开关打开的情况下，老师**全程不用喊一声**。谁该上台、谁该准备，系统比谁都清楚。

### 座位长什么样

- 讲台正前方有 **2 个位置**
- 后面是 **4 个大组**，每组 **7 排**，每排 **2 人**（左、右）
- 座位编号长这样：`3组5排左`，也就是组号 + 排号 + 左/右
- 第 1 大组在教室**最右侧**

> 顺便记住：别人的位置你**看不到姓名**，只会看到一把小锁头 🔒。这是故意的，不用担心。

---

## 二、被叫到号之后怎么做

听到自己名字就上台，走到大屏幕前。下面三步，全班每个人都一样。

叫到谁，右上角就写谁的名字。屏幕上一排空座位都是可以点的，你随便挑一个。

1. 听到自己名字，走上台
2. 看屏幕，**点一个空座位**（显示 `⬚` 的那个）
3. 坐下就行，**不用再点别的**，系统会自动叫下一位

点完坐下就行。系统立刻自动跳到下一位同学并喊他上台，右边「已完成选座」同步记录。

> 被占用的座位点不动，会自动跳过；老师关掉的位置也点不了。实在选不到，喊老师帮你安排。

**同班同学能坐同桌吗**

老师可能开放「指定同桌」权限。开放之后，你点座位时会问你一句要不要和某位同学坐一起，**要对方同意才生效**。没开放就不用管这一条。

---

## 三、锦上添花：提前填志愿

> 这一节是**可选的**。前面的主流程不填志愿也能完整跑完。填志愿只解决一件事：**你那天不在场**。

比如你要请假、出去比赛那天，人来不了。提前把志愿填好，系统会照着你的志愿顺序自动帮你坐，**不用到场**。想更快的话，全班都填好，老师连叫号都能省。

### 怎么填

1. 用**学生**身份登录（`姓名`或**拼音首字母**，比如输 `c` 列出所有姓陈的同学）
2. 点空座位加进「我的志愿」，**最多 10 个**；再点一次取消
3. 在面板里**拖动调整顺序**，数字 1 是最想坐的位置；不想要了拖到 🗑️ 删除

<img width="1440" height="900" alt="01-login" src="https://github.com/user-attachments/assets/604ac502-ff2b-4426-a3bf-968c4e3edef9" />


点「🎓 学生」，然后输入姓名或拼音首字母。第一次用会让你设一个密码。

<img width="1440" height="900" alt="wish-drag" src="https://github.com/user-attachments/assets/7d624c77-cbee-4526-8ab6-4a98cb0bedd0" />


座位上的粉色数字和面板里的数字对应，一眼看出自己填了哪些位置、第几顺位。

正在拖动第 1 个志愿，落到第 3 个上会变成琥珀色，松手就交换顺序。

### 系统怎么用你的志愿

1. 最多 **10 个**志愿。
2. 按你填的顺序 **1 → 10 依次尝试**。
3. 位置**已经有人**或**被老师关掉** → 自动跳过。
4. 找到第一个能用的就**停下**，后面的不再看。
5. 10 个都不行 → 告诉老师手动安排，**不会漏掉任何人**。

<img width="760" height="646" alt="algo-flow" src="https://github.com/user-attachments/assets/3a6fa59f-b5b0-41b7-bd3a-e03213595206" /><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 760 646" width="760" height="646" font-family="ui-monospace, 'SF Mono', Menlo, Consolas, monospace">
  <defs>
    <pattern id="g2" width="24" height="24" patternUnits="userSpaceOnUse">
      <path d="M24 0H0V24" fill="none" stroke="#6f9fb5" stroke-opacity="0.13" stroke-width="1"/>
    </pattern>
    <pattern id="g2m" width="120" height="120" patternUnits="userSpaceOnUse">
      <rect width="120" height="120" fill="url(#g2)"/>
      <path d="M120 0H0V120" fill="none" stroke="#6f9fb5" stroke-opacity="0.22" stroke-width="1.2"/>
    </pattern>
    <marker id="cy" markerWidth="9" markerHeight="9" refX="8" refY="4.5" orient="auto">
      <path d="M0,0 L9,4.5 L0,9 Z" fill="#7fb2cc"/>
    </marker>
    <marker id="am" markerWidth="9" markerHeight="9" refX="8" refY="4.5" orient="auto">
      <path d="M0,0 L9,4.5 L0,9 Z" fill="#f0b429"/>
    </marker>
  </defs>

  <rect width="760" height="646" fill="#151d33"/>
  <rect width="760" height="646" fill="url(#g2m)"/>
  <rect x="14" y="14" width="732" height="618" fill="none" stroke="#4a7091" stroke-opacity="0.5"/>

  <!-- title -->
  <text x="30" y="42" fill="#e8f4fa" font-size="17" font-weight="700" letter-spacing="0.5">排座算法流程</text>
  <text x="30" y="62" fill="#7fb2cc" font-size="12">FIG.02  老师点「下一名」后，系统对每位同学做的事</text>
  <text x="730" y="42" fill="#7fb2cc" font-size="12" text-anchor="end">⊞ A-02</text>
  <line x1="30" y1="74" x2="730" y2="74" stroke="#4a7091" stroke-opacity="0.6"/>

  <!-- STEP 0 -->
  <rect x="270" y="94" width="220" height="46" fill="#1e2b47" stroke="#7fb2cc" stroke-width="1.4"/>
  <text x="380" y="114" fill="#cfe6f2" font-size="13" font-weight="700" text-anchor="middle">老师点「▶ 下一名」</text>
  <text x="380" y="132" fill="#8fb8cc" font-size="11.5" text-anchor="middle">取出下一位还没选座的同学</text>
  <line x1="380" y1="140" x2="380" y2="168" stroke="#7fb2cc" stroke-width="1.5" marker-end="url(#cy)"/>

  <!-- decision: has wish -->
  <path d="M380 172 L500 208 L380 244 L260 208 Z" fill="#1b2b4a" stroke="#7fb2cc" stroke-width="1.5"/>
  <text x="380" y="205" fill="#e8f4fa" font-size="13.5" font-weight="700" text-anchor="middle">他填志愿了吗？</text>
  <text x="380" y="223" fill="#8fb8cc" font-size="11" text-anchor="middle">最多 10 个</text>

  <!-- NO branch -> call up -->
  <text x="270" y="272" fill="#ffd970" font-size="12.5" font-weight="700" text-anchor="end">没有</text>
  <path d="M262 208 L150 208 L150 300" fill="none" stroke="#f0b429" stroke-width="1.5" marker-end="url(#am)"/>
  <rect x="46" y="302" width="208" height="52" fill="#2a2410" stroke="#f0b429" stroke-width="1.4"/>
  <text x="150" y="323" fill="#ffd970" font-size="12.5" font-weight="700" text-anchor="middle">老师喊他上台</text>
  <text x="150" y="342" fill="#c9b183" font-size="11" text-anchor="middle">他自己点一个空座位</text>

  <!-- YES branch -> wish loop -->
  <text x="516" y="200" fill="#7fb2cc" font-size="12.5" font-weight="700">填了</text>
  <path d="M498 208 L600 208 L600 288" fill="none" stroke="#7fb2cc" stroke-width="1.5" marker-end="url(#cy)"/>

  <!-- wish scan box -->
  <rect x="500" y="290" width="212" height="150" fill="#182742" stroke="#7fb2cc" stroke-width="1.4"/>
  <text x="606" y="312" fill="#cfe6f2" font-size="12.5" font-weight="700" text-anchor="middle">按顺序 1 → 10 逐个找</text>
  <line x1="514" y1="322" x2="698" y2="322" stroke="#4a7091" stroke-opacity="0.7"/>

  <text x="516" y="342" fill="#a8c4d6" font-size="11.5">① 这个位置空着吗？</text>
  <text x="528" y="360" fill="#8fb8cc" font-size="11">不空（有人/被关掉）</text>
  <text x="528" y="377" fill="#8fb8cc" font-size="11">→ 换下一个</text>
  <text x="516" y="398" fill="#a8c4d6" font-size="11.5">② 空着 → 就坐这儿</text>
  <text x="528" y="416" fill="#8fb8cc" font-size="11">后面的志愿不再看</text>
  <text x="516" y="434" fill="#a8c4d6" font-size="11.5">③ 10 个都不行 → 转右边</text>

  <!-- loop back arrow -->
  <path d="M500 340 L470 340 L470 430 L494 430" fill="none" stroke="#7fb2cc" stroke-opacity="0.75" stroke-width="1.2" marker-end="url(#cy)"/>
  <text x="466" y="392" fill="#7fb2cc" font-size="10.5" text-anchor="end">继续试</text>

  <!-- decision: found -->
  <path d="M606 458 L700 490 L606 522 L512 490 Z" fill="#1b2b4a" stroke="#7fb2cc" stroke-width="1.5"/>
  <text x="606" y="488" fill="#e8f4fa" font-size="13" font-weight="700" text-anchor="middle">找到空位了？</text>
  <text x="606" y="506" fill="#8fb8cc" font-size="11" text-anchor="middle">或 10 个都试完</text>

  <!-- FOUND -> seat -->
  <text x="716" y="478" fill="#ffd970" font-size="12.5" font-weight="700" text-anchor="end">找到</text>
  <path d="M698 490 L640 490 L640 542" fill="none" stroke="#f0b429" stroke-width="1.5" marker-end="url(#am)"/>
  <rect x="530" y="544" width="212" height="50" fill="#2a2410" stroke="#f0b429" stroke-width="1.5"/>
  <text x="636" y="565" fill="#ffd970" font-size="13" font-weight="700" text-anchor="middle">自动落座</text>
  <text x="636" y="584" fill="#c9b183" font-size="11" text-anchor="middle">人不在场也能坐</text>

  <!-- NOT FOUND -> teacher -->
  <path d="M606 522 L606 542 L300 542 L300 574 L266 574" fill="none" stroke="#f0b429" stroke-width="1.5" marker-end="url(#am)"/>
  <text x="470" y="536" fill="#ffd970" font-size="12.5" font-weight="700">10 个都不行</text>

  <rect x="46" y="550" width="212" height="50" fill="#2a2410" stroke="#f0b429" stroke-width="1.4"/>
  <text x="152" y="570" fill="#ffd970" font-size="12.5" font-weight="700" text-anchor="middle">老师手动安排</text>
  <text x="152" y="589" fill="#c9b183" font-size="11" text-anchor="middle">不会漏掉任何人</text>

  <!-- footer -->
  <line x1="30" y1="610" x2="730" y2="596" stroke="#4a7091" stroke-opacity="0.6"/>
  <text x="30" y="625" fill="#9fc4d8" font-size="11.5">两条路殊途同归：不管哪种方式，最后都坐在教室里的同一个座位上</text>
</svg>


这位同学的第 1 志愿已经被人占了，系统自动往下试，落到第 2 个志愿。全程没人到场。

---

## 四、可能被问到的问题

**Q：我能选到哪个位置？**
按学校公布的顺序，轮到你时，**任何空座位你都可以点**。

**Q：一定要上台吗？**
不一定。填了志愿的话，你人不在场系统也能自动安排；没填就来现场点一下。

**Q：志愿会不会白填？**
不会。你人不在场时，系统就自动按你填的顺序找位置。

**Q：我能跟朋友坐同桌吗？**
可以给对方发邀请，但**要对方同意才生效**。老师也可能开放「指定同桌」的权限。

**Q：填满 10 个了还能改吗？**
能。删掉不要的，再补上想要的就行。

**Q：我能看见别人的名字吗？**
不能。你只能看到哪些位置已经有人（显示 🔒），看不到是谁。这样大家都是同一起跑线。

---

## 五、给老师：怎么把全班排完

1. **导入名单**：Excel / CSV 一次导入
2. **导入优先级**：把顺序排好直接导进去
3. **打开语音开关**：让系统自动叫号
4. **叫下一个名字**：老师不用动手，等学生自己走上来点
5. **选完导出 CSV**：留一份备份

---

有问题找班主任。

---

*本文档对应的 Markdown 版与 HTML 版在项目 `docs/` 目录下。*
