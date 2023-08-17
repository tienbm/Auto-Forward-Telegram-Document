# Add Header / Footer

{% hint style="info" %}
You can add a header or footer for each post when forward to channels target
{% endhint %}

{% tabs %}
{% tab title="Instructions" %}
To reach this first you will need to type **/settings** on **Auto Forward Telegram BOT.** Now click on **work1** so you can access the setup settings. Finally the **Add Header or Add Footer** ➡️&#x20;

Enter content you want show with some options
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Options Explained" %}
📖 Some formats you can refer to:

&#x20; ➡️  **Enter EMPTY if you don't want to show the header.**&#x20;

&#x20; ➡️ **\n** if you want break line.

&#x20; ➡️ **\t** if you want spaces.

&#x20; ➡️ **\[\[ORIGIN\_USERNAME]]** if you want to show the sender username

&#x20; ➡️ **\[\[ORIGIN\_USERID]]** if you want to show the sender userid

&#x20; ➡️ **\[\[ORIGIN\_TEXT]]** if you want to show original content.&#x20;

&#x20; ➡️ **\[\[ORIGIN\_NAME]]** if you want to show the sender name or name original channel.&#x20;

&#x20; ➡️ **\[\[ORIGIN\_POST\_ID]]** if you want show Post ID origin.&#x20;

&#x20; ➡️ **\[\[ORIGIN\_CHAT\_ID]]** if you want show CHAT ID origin.

&#x20; ➡️ **\[\[ORIGIN\_QUOTED\_TEXT]]** if you want to display the original post's QUOTED TEXT.

&#x20; ➡️ **\[\[ORIGIN\_NAME\_URL]]** if you want to show the original link.

&#x20; ➡️ **\[\[FROM\_USER]]** if you want to show the username of sender.

&#x20; ➡️ **\[\[SOURCE\_NAME]]** if you want to show forward source name.

&#x20; ➡️ **\[\[SENDER\_CHAT]]** if you want to show name display of sender.

&#x20; ➡️ **\[\[FORWARD\_FROM\_CHAT]]** if you want to show message owner name
{% endtab %}
{% endtabs %}



{% tabs %}
{% tab title="Example Header" %}
✏️ **Add Header with format as**

Content: \[\[ORIGIN\_TEXT]]

From channel: \[\[ORIGIN\_NAME]]

ID: \[\[ORIGIN\_POST\_ID]]

CHAT\_ID: \[\[ORIGIN\_CHAT\_ID]]&#x20;

\n

➡️ **Result after forward content "Hello":**

Content: Hello&#x20;

From channel: Source chat test 2&#x20;

ID: 4232&#x20;

CHAT\_ID: 1656164752



Hello
{% endtab %}

{% tab title="Example Footer" %}
✏️ **Add Footer with format as**

**-----**signature**------**

From channel: \[\[ORIGIN\_NAME]]

ID: \[\[ORIGIN\_POST\_ID]]

CHAT\_ID: \[\[ORIGIN\_CHAT\_ID]]&#x20;

\n

➡️ **Result after forward content "Hello":**

Hello

**-----**signature**------**

From channel: Source chat test 2&#x20;

ID: 4232&#x20;

CHAT\_ID: 1656164752
{% endtab %}
{% endtabs %}



