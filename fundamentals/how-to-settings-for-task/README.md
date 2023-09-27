# 🛠 How To Settings For Task

{% hint style="info" %}
This is list menu for task settings such as **Edit Source Chat, Edit Target Chat or Delete Task or Advanced Configuration and more**
{% endhint %}

**Use command to get and access to Task**

{% hint style="success" %}
**/settings** or **/forward**
{% endhint %}

{% tabs %}
{% tab title="Instructions" %}
**1.** After typing the command, select **Manage Forwarding Tasks** or **Show ALL** to show all your list Task.\
**2.** Next click a **Task**  you want settings.
{% endtab %}
{% endtabs %}

<figure><img src="../../.gitbook/assets/image (69).png" alt=""><figcaption><p>Setting Task</p></figcaption></figure>

{% tabs %}
{% tab title="Options Explained" %}
* **Edit Source Chat :** Change the current source ids of the task
* **Edit Source Chat :** Change the current target ids of the task
* **Delete Task:** Remove Task
* **Edit Delay :** Specify the delay (in seconds) you'd like between forwarded messages for your task.
* **Edit Max Time Edit :** Specify the maximum time (in seconds) allowed for editing a message in your task.
* **Advanced Configuration:** Config advanced features for task forward
{% endtab %}
{% endtabs %}



### **Advanced Configuration**

<figure><img src="../../.gitbook/assets/image (70).png" alt=""><figcaption><p><strong>Advanced Configuration</strong></p></figcaption></figure>

{% tabs %}
{% tab title="Options Explained" %}
* **Show Header Forwarder :** check ✅ if you want all your messages will be prefixed with "Forwarded from ...".&#x20;

&#x20;      ️➡️ _<mark style="color:red;">**Note: if you turn on the feature**</mark>_<mark style="color:red;">** **</mark><mark style="color:red;">**Show Header Forwarder**</mark><mark style="color:red;">** **</mark>_<mark style="color:red;">**then features Reply, Edit, Replace,**</mark>_<mark style="color:red;">** **</mark><mark style="color:red;">**translate**</mark><mark style="color:red;">** **</mark>_<mark style="color:red;">**will not work.**</mark>_

* **Duplicate Filters:** check ✅ if you want to **block duplicate messages** from forwarding.
* **Replace:** click ➡️ if you want to replace word feature to work on this task
* **Black List:** click ➡️ if you want to Allow Blacklist feature to work on this task
* **White List:** click ➡️ if you want to Allow Whitelist feature to work on this task
* **Filter:** click ➡️ if you want to used to filter messages by type feature to work on this task
* **Cleaner:** click ➡️ if you want to clean text, video, photo...etc from message on this task
* **Filter Users:** click ➡️ if you want to **Allow Whitelist users id** feature to work on this task
* **Scheduler Power On/Off** click ➡️ if you want to schedule on/off task
* **Auto Post Scheduler** click ➡️ if you want to schedule auto forward post last on task
* **Translate Language** click ➡️ if you want translate a post message to language other
* **Crypto Filters** click ➡️ if you only want receive crypto address
* **Process To Raw Text** click ➡️ if you only want receive raw post
* **Convert Buttons To Text** click ➡️ if you want convert post contain button to text
* **Add Header:** click it if you want add header text before every message on this task
* **Add Footer:** click it if you want add footer text after every message on this task
* **Reply:** check ✅ if you want to properly **process replies**\
  Note, if you enable the "**Show Header Forwarder**" feature, the reply function will not work, it will be sent as **a new message** by default.
* **Edit:** check ✅ if you want to edit messages if they got edited in the **SOURCE\_ID**\
  If check 🚫 then All edit message from **SOURCE\_ID** will not be edited on your **TARGET\_ID** and will sent as **new messages**
* **Delete:** check ✅ if you want to remove messages if they got removed in the **SOURCE\_ID**\
  Note, if you enable the "**Show Header Forwarder**" feature, the delete function will not work
{% endtab %}
{% endtabs %}

