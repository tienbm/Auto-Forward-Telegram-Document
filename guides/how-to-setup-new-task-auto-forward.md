# 💫 How To Setup New Task Auto Forward

### ⛳️ Create New Task

{% tabs %}
{% tab title="Command" %}
**Use the following syntax for adding channels/users/bots:**\
`/forward add [LABEL] [SOURCE_CHAT_ID] -> [TARGET_CHAT_ID]`

**Command other**

`/forward remove [LABEL]`

`/forward start [LABEL]`

`/forward stop [LABEL]`
{% endtab %}

{% tab title="Example" %}
**One to One**\
`/forward add work1 22222 -> 66666`\
\
**Many to One**\
`/forward add work1 22222,33333 -> 66666`\
\
**One to Many**\
`/forward add work1 22222 -> 66666,77777`\
\
**Many to Many**\
`/forward add work1 22222,33333 -> 66666,77777`\
\
\===============\
\
**Remove task with label work1 in list**\
`/forward remove work1`\
\
**Start task with label work1 in list**\
`/forward start work1`\
\
**Stop task with label work1 in list**\
`/forward stop work1`\


**Set delay 30 seconds to each message with label work1** \
`/forward delay work1 30`\


**Set maximum time limit to receive message edit event from SOURCE\_ID is 30 seconds with label work1** \
`/forward max_time_edit work1 30`

\
**Restart all process if any error**\
`/forward restart`\
\
**Show all list task**\
`/forward task`
{% endtab %}
{% endtabs %}

{% hint style="success" %}
**Command Information**

* **`SOURCE_CHAT_ID`**` ``and`` `**`TARGET_CHAT_ID`**get from command [**/getchanel**](get-information-channels-groups-your-account.md) or [**/getgroup**](get-information-channels-groups-your-account.md) or [**/getuser**](get-information-channels-groups-your-account.md)
* You can only use source and target id's you find via [**/getchanel**](get-information-channels-groups-your-account.md) or [**/getgroup**](get-information-channels-groups-your-account.md) or [**/getuser**](get-information-channels-groups-your-account.md)
* **LABEL** is the nickname you want to define for your Task. This variable is used setup later on every **Auto Forward Telegram BOT** command.
* Do not use number id you give from **/getchanel** or **/getgroup** or **/getuser** for LABEL.&#x20;
{% endhint %}

{% embed url="https://drive.google.com/file/d/1HFTw-AH5dLrt6K9YfiCpy5DGcCJ75UqE/view?usp=sharing" %}
Get **`SOURCE_CHAT_ID`** and **`TARGET_CHAT_ID`**
{% endembed %}

![Use it as CHAT\_ID or TARGET\_ID](<../.gitbook/assets/image (33).png>)

{% embed url="https://www.youtube.com/watch?v=umCVIHbO-SU" %}
Video create a new Task
{% endembed %}

### 🛠 Management Task (Settings, Delete, Edit)

Use Command **/forward** then select **Show All**

<figure><img src="../.gitbook/assets/ezgif-1-69d3e23ecc.gif" alt=""><figcaption><p>Manage Task</p></figcaption></figure>

