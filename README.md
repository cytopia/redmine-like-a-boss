# Redmine lik a boss

Easy redmine plugin/theme management via git submodules and symlinks.

Use `redmine-lile-a-pro.sh` to list available plugins and themes and enable/disable as desired. You don't need to worry about database up/down migrations or additional install builds as it is handled automatically (See [plugin.ini](https://github.com/cytopia/redmine-like-a-boss/blob/master/redmine-plugins/plugin.ini) for plugin configuration.

When plugins are chosen to be enabled, they are simply symlinked to the proper redmine plugins directory and all required tasks (db migrations, builds etc) are done afer your explicit OK.

When plugins are chosen to be disabled, required tasks are run (down migrations) and the symlink is simply removed. The plugin directory will still be there waiting to be enabled again.

Plugin updates are simple too, as you only need to `git pull` in the appropriate git submodule repository.


## Available Plugins

* Issuefy (issuefy)
* Line numbers (line_numbers)
* Progressive Projects List (progressive_projects_list)
* Recurring Tasks (recurring_tasks)
* Redmine Agile (redmine_agile)
* Redmine Announcements (redmine_announcements)
* Redmine Checklists (redmine_checklists)
* Redmine CMS (redmine_cms)
* Redmine CRM (redmine_contacts)
* Redmine Dashboard (redmine_dashboard)
* Did You Mean Plugin (redmine_didyoumean)
* Redmine Document Management System (redmine_dmsf)
* Redmine Favorite projects (redmine_favorite_projects)
* Redmine Finance (redmine_finance)
* Redmine Gist (redmine_gist)
* Project Search Box Plugin (redmine_improved_searchbox)
* Redmine Issues Tree (redmine_issues_tree)
* Redmine My Page Customization (redmine_my_page)
* Redmine People (redmine_people)
* Redmine Planning (redmine_planning)
* Redmine Q&A plugin (redmine_questions)
* Redmine Tags (redmine_tags)
* Redmine Tweaks (redmine_tweaks
* Redmine Zen Edit (redmine_zenedit)
* Hide Sidebar (sidebar_hide)
* Unread issues (unread_issues)

## Usage

### Main Menu
```shell
------------------------------------------------------------
-                  Redmine like a boss                     -
------------------------------------------------------------

What do you want to do?

   2. List/check plugins
   3. Enable plugin
   4. Disable plugin

   9. Exit program

Enter a number between 1-9: 2
```
### List menu
```shell
                  Redmine like a boss                     -
------------------------------------------------------------

Available plugins (26)

 1 Issuefy (issuefy) (0.2.0) (Enabled)
 2 Line numbers (line_numbers) (1.0.0)
 3 Progressive Projects List (progressive_projects_list) (3.0.1)
 4 Recurring Tasks (recurring_tasks) (1.6.0)
 5 Redmine Agile (redmine_agile) (1.4.0)
 6 Redmine Announcements (redmine_announcements) (1.3.0)
 7 Redmine Checklists (redmine_checklists) (3.1.3)
 8 Redmine CMS (redmine_cms) (0.0.3)
 9 Redmine CRM (redmine_contacts) (4.0.4)
10 Redmine Dashboard (redmine_dashboard) (2.7.0)
11 Did You Mean Plugin (redmine_didyoumean) (1.2.0)
12 Redmine Document Management System (redmine_dmsf) (1.5.6)
13 Redmine Favorite projects (redmine_favorite_projects) (1.0.1)
14 Redmine Finance (redmine_finance) (2.0.1)
15 Redmine Gist (redmine_gist) (0.1.0)
16 Project Search Box Plugin (redmine_improved_searchbox) (0.0.3)
17 Redmine Issues Tree (redmine_issues_tree) (0.0.6)
18 Redmine My Page Customization (redmine_my_page) (0.1.9)
19 Redmine People (redmine_people) (1.2.0)
20 Redmine Planning (redmine_planning) (1.0.0)
21 Redmine Q&A plugin (redmine_questions) (0.0.7)
22 Redmine Tags (redmine_tags) (3.1.1)
23 Redmine Tweaks (redmine_tweaks) (0.5.7)
24 Redmine Zen Edit (redmine_zenedit) (0.0.2)
25 Hide Sidebar (sidebar_hide) (0.0.7)
26 Unread issues (unread_issues) (0.0.1)

Press any key to continue...
```

### Enable menu
```shell
------------------------------------------------------------
-                  Redmine like a boss                     -
------------------------------------------------------------

Plugins that can be enabled

 1 Line numbers (1.0.0)
 2 Progressive Projects List (3.0.1)
 3 Recurring Tasks (1.6.0)
 4 Redmine Agile (1.4.0)
 5 Redmine Announcements (1.3.0)
 6 Redmine Checklists (3.1.3)
 7 Redmine CMS (0.0.3)
 8 Redmine CRM (4.0.4)
 9 Redmine Dashboard (2.7.0)
10 Did You Mean Plugin (1.2.0)
11 Redmine Document Management System (1.5.6)
12 Redmine Favorite projects (1.0.1)
13 Redmine Finance (2.0.1)
14 Redmine Gist (0.1.0)
15 Project Search Box Plugin (0.0.3)
16 Redmine Issues Tree (0.0.6)
17 Redmine My Page Customization (0.1.9)
18 Redmine People (1.2.0)
19 Redmine Planning (1.0.0)
20 Redmine Q&A plugin (0.0.7)
21 Redmine Tags (3.1.1)
22 Redmine Tweaks (0.5.7)
23 Redmine Zen Edit (0.0.2)
24 Hide Sidebar (0.0.7)
25 Unread issues (0.0.1)

Enter the number of plugin to enable or 'q' to abort: 1
Symlink "Line numbers" (line_numbers) to Redmin plugin directory? (Y/n)y
Update Redmine bundles? (Y/n)y
Bundle updated!
Install potentiel new Redmine bundles? (Y/n)y
"Line numbers" does not require builds.
"Line numbers" does not require database migrations.

"Line numbers" installed. Restart Redmine

Press any key to continue...
```

## Contribution

Feel free to add more plugins.
