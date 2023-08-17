# 🧙♂ Filter Users

{% hint style="info" %}
You can set a list of user id s to tell the bot to process messages you receive from source group only if it matches at least one of the user id's on the list.

🛑 **This feature work only for group**
{% endhint %}

{% tabs %}
{% tab title="Command" %}
Command Arguments\
`/filter_users ACTION LABEL LIST_USER_ID`

\==============

**HOW TO FIND a USER ID**

Use bot [@getidsbot](https://t.me/getidsbot) => Click Start&#x20;

Afterward forward any post message of user you want get ID from any channel/group/chat into this bot
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Example" %}
*   For Example

    ➡️ This will only allow messages from user\_id **123456** to be forwarded to **TARGET\_ID** with label **user1** \
    `/filter_users add user1 123456`

    ➡️ This will only allow messages from user\_id **123456** or **565656** or **232323** to be forwarded to **TARGET\_ID** with label **user1** \
    `/filter_users add user1 123456,565656,232323`

    ➡️ Remove list user with label **user1** \
    `/filter_users remove user1`

    Show all filter users list \
    `/filter_users showall`
{% endtab %}
{% endtabs %}

![](../.gitbook/assets/ezgif-4-f7420a2f1b.gif)

### ✅ Apply/Disable Filter Users For a Task

{% hint style="warning" %}
Please [disable Filter User All ](filter-users.md#apply-disable-filter-users-for-all-task)before apply for a task
{% endhint %}

Use command **/setting** after select **Task** want apply

![](../.gitbook/assets/ezgif-4-03421fd62d.gif)

### ✅ Apply/Disable Filter Users For All Task

{% hint style="danger" %}
When **Apply All Filter Users for Task** will won't activate for each single task
{% endhint %}

Use command **/filter\_users** after select **Show All Filter Users**

![](../.gitbook/assets/ezgif-4-702ca3eabd.gif)

### ✅ Remove All **Filter Users**

Use command **/filter\_users** after select **Remove All Filter Users**

![](../.gitbook/assets/ezgif-4-8ee53dd908.gif)
