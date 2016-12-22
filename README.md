# mod_chatpage

Zotonic chat module, chat in the context of a resource. Adds chat to the admin.

Usage
-----

After the module has been installed (see below) this adds chat in the context of a page.

The chat is coupled to the page and has optional *sub-chats*.
The default sub-chat is *default*. Other options are modules based chats where
the sub-chat is called after the module, for example *mod_admin*.

This module adds two special resources:

 * The category *chatpage*
 * A page of the category chatpage to be used for *admin chats*

The name of the admin chat page is `page_admin_chatpage`.

Check the `page.chatpage.tpl` template for the structure of the html.

Admin Chat
----------

In the admin the chat window will be on the right and opens automatically if a message is received.

On an edit page there are two possible chats, the chat for the page and the chat for all admin users.
When editing a page the page chat will be shown, but it will switch to the shared admin-users chat.

This can also be done by selecting it from the select element.

![Admin Chat Example](https://github.com/mworrell/mod_chatpage/raw/master/doc/admin-chat.png)


Installation
------------

Install this module like all other modules in `user/modules`.
Ensure that the module is enabled and the the access controls are set correctly.

Every user wanting to chat must have *use* rights on *mod_chatpage*.
Users having this right and also access to the admin will see the chat menu on the right.


Known problems
--------------

The presence of an user is not always communicated correctly on page unload.
This can leave some users seemingly online for a couple of seconds after they left the page.


Future changes
--------------

This module will be adapted so that it can be used with the future Zotonic component system.
