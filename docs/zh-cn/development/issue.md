## 前言
Issues 功能被用来追踪各种特性，Bug，功能等。项目维护者可以通过 Issues 来组织需要完成的任务。

Issue 是引出一个 Feature 或 Bug 等的重要步骤，在单个
Issue 中可以讨论的内容包括但不限于 Feature 的包含的功能，存在的 Bug 产生原因，前期方案的调研，以及其对应的实现设计和代码思路。

并且只有当 Issue 被 approve 之后才需要有对应的 Pull Request 去实现。

如果是一个 Issue 对应的是一个大 Feature，建议先将其按照功能模块等维度分成多个小的 Issue。

## 规范

### Issue 标题

标题格式：[`Issue 类型`][`模块名`] `Issue 描述`

其中`Issue 类型`如下：

<table>
    <thead>
        <tr>
            <th style="width: 10%; text-align: center;">Issue 类型</th>
            <th style="width: 20%; text-align: center;">描述</th>
            <th style="width: 20%; text-align: center;">样例</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: center;">Feature</td>
            <td style="text-align: center;">包含所期望的新功能和新特性</td>
            <td style="text-align: center;">[Feature][api] Add xxx api in xxx controller</td>
        </tr>
        <tr>
            <td style="text-align: center;">Bug</td>
            <td style="text-align: center;">程序中存在的 Bug</td>
            <td style="text-align: center;">[Bug][api] Throw exception when xxx</td>
        </tr>
        <tr>
            <td style="text-align: center;">Improvement</td>
            <td style="text-align: center;">针对目前程序的一些改进，不限于代码格式，程序性能等</td>
            <td style="text-align: center;">[Improvement][server] Improve xxx between Master and Worker</td>
        </tr>
        <tr>
            <td style="text-align: center;">Test</td>
            <td style="text-align: center;">专门针对测试用例部分</td>
            <td style="text-align: center;">[Test][server] Add xxx e2e test</td>
        </tr>
        <tr>
            <td style="text-align: center;">Sub-Task</td>
            <td style="text-align: center;">一般都是属于 Feature 类的子任务，针对大 Feature，可以将其分成很多个小的子任务来一一完成</td>
            <td style="text-align: center;">[Sub-Task][server] Implement xxx in xxx</td>
        </tr>
    </tbody>
</table>

其中`模块名`如下：

<table>
    <thead>
        <tr>
            <th style="width: 10%; text-align: center;">模块名</th>
            <th style="width: 20%; text-align: center;">描述</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: center;">alert</td>
            <td style="text-align: center;">报警模块</td>
        </tr>
        <tr>
            <td style="text-align: center;">api</td>
            <td style="text-align: center;">应用程序接口层模块</td>
        </tr>
        <tr>
            <td style="text-align: center;">service</td>
            <td style="text-align: center;">应用程序服务层模块</td>
        </tr>
        <tr>
            <td style="text-align: center;">dao</td>
            <td style="text-align: center;">应用程序数据访问层模块</td>
        </tr>
        <tr>
            <td style="text-align: center;">plugin</td>
            <td style="text-align: center;">插件模块</td>
        </tr>
        <tr>
            <td style="text-align: center;">remote</td>
            <td style="text-align: center;">通信模块</td>
        </tr>
        <tr>
            <td style="text-align: center;">server</td>
            <td style="text-align: center;">服务器模块</td>
        </tr>
        <tr>
            <td style="text-align: center;">ui</td>
            <td style="text-align: center;">前端界面模块</td>
        </tr>
        <tr>
            <td style="text-align: center;">docs-zh</td>
            <td style="text-align: center;">中文文档</td>
        </tr>
        <tr>
            <td style="text-align: center;">docs</td>
            <td style="text-align: center;">英文文档</td>
        </tr>
        <tr>
            <td style="text-align: center;">待补充...</td>
            <td style="text-align: center;">-</td>
        </tr>
    </tbody>
</table>

### Issue 内容模板

https://github.com/apache/incubator-dolphinscheduler/tree/dev/.github/ISSUE_TEMPLATE

### Contributor

除一些特殊情况之外，在开始完成
Issue 之前，建议先在 Issue 下或者邮件列表中和大家讨论确定设计方案或者提供设计方案，以及代码实现思路。

如果存在多种不同的方案，建议通过邮件列表或者在
Issue 下进行投票决定，最终方案和代码实现思路被
approve 之后，再去实现，这样做的主要目的是避免在
Pull Request review 阶段针对实现思路的意见不同或需要重构而导致 waste time。

### 相关问题

- 当出现提出 Issue 的用户不清楚该 Issue 对应的模块时的处理方式。

    确实存在大多数提出 Issue 用户不清楚这个 Issue 是属于哪个模块的，其实这在很多开源社区都是很常见的。在这种情况下，其实
    committer/contributor 是知道这个 Issue 影响的模块的，如果之后这个 Issue 被 committer 和 contributor approve
    确实有价值，那么 committer 就可以按照 Issue 涉及到的具体的模块去修改 Issue 标题，或者留言给提出 Issue 的用户去修改成对应的标题。