# Redmine lik a boss

Easy redmine plugin/theme management via git submodules and symlinks.

Use `redmine-lile-a-boss.sh` to list available plugins and themes and enable/disable as desired. You don't need to worry about database up/down migrations or additional install builds as it is handled automatically (See [plugin.ini](https://github.com/cytopia/redmine-like-a-boss/blob/master/redmine-plugins/plugin.ini) and [theme.ini](https://github.com/cytopia/redmine-like-a-boss/blob/master/redmine-themes/theme.ini) for plugin/theme configuration.

---

**STAY UP TO DATE**

```shell
git pull origin master
git submodule update --recursive
```

---

### How does it work?

#### Installation (enable)

When plugins are chosen to be enabled, they are simply symlinked to the proper redmine plugins directory and all required tasks (db migrations, builds etc) are done afer your explicit OK.

#### Uninstallation (disable)

When plugins are chosen to be disabled, required tasks are run (down migrations) after your explicit OK and only the symlink is removed. The plugin directory itself will still remain untouched, ready to be enabled again.

#### Updates (git pull)

Plugin updates are simple too, as you only need to `git pull` in the appropriate git submodule repository.

#### Manually

You can also use this repository and still do everything manually. All you need to do by hand is symlink the plugin/theme to the redmine directory and run potential database migrations.



## 1. Available git modules

### 1.1 Redmine

* Redmine ([redmine](https://github.com/redmine/redmine)) 3.2.1

Redmine is included as a git submodule from the official repository currently in version `3.2.1`. This repository will always add the latest stable version so you only need to update `redmine-like-a-boss`.
You can however checkout any version you like within the submodule to fit your needs.

### 1.2 Available Plugins

See [plugin.ini](https://github.com/cytopia/redmine-like-a-boss/blob/master/redmine-plugins/plugin.ini) for description, license, author and version information.

* Issuefy ([issuefy](https://github.com/tchx84/issuefy))
* Line numbers ([line_numbers](https://github.com/cdwertmann/line_numbers))
* Progressive Projects List ([progressive_projects_list](https://github.com/stgeneral/redmine-progressive-projects-list))
* Recurring Tasks ([recurring_tasks](https://github.com/nutso/redmine-plugin-recurring-tasks))
* Redmine Agile ([redmine_agile](https://github.com/RCRM/redmine_agile))
* Redmine Announcements ([redmine_announcements](https://github.com/buoyant/redmine_announcements))
* Redmine Checklists ([redmine_checklists](https://github.com/RCRM/redmine_checklists))
* Redmine CMS ([redmine_cms](https://github.com/RCRM/redmine_cms))
* Redmine CRM ([redmine_contacts](https://github.com/RCRM/redmine_contacts))
* Redmine Dashboard ([redmine_dashboard](https://github.com/jgraichen/redmine_dashboard))
* Did You Mean Plugin ([redmine_didyoumean](https://github.com/abahgat/redmine_didyoumean))
* Redmine Document Management System ([redmine_dmsf](https://github.com/danmunn/redmine_dmsf))
* Redmine Favorite projects ([redmine_favorite_projects](https://github.com/RCRM/redmine_favorite_projects))
* Redmine Finance ([redmine_finance](https://github.com/RCRM/redmine_finance))
* Redmine Gist ([redmine_gist](https://github.com/dergachev/redmine_gist))
* Project Search Box Plugin ([redmine_improved_searchbox](https://github.com/ries-tech/redmine_improved_searchbox))
* Redmine Issues Tree ([redmine_issues_tree](https://github.com/Loriowar/redmine_issues_tree))
* Redmine My Page Customization ([redmine_my_page](https://github.com/jrupesh/redmine_my_page))
* Redmine People ([redmine_people](https://github.com/RCRM/redmine_people))
* Redmine Planning ([redmine_planning](https://github.com/MadEgg/redmine_planning))
* Redmine Q&A plugin ([redmine_questions](https://github.com/RCRM/redmine_questions))
* Redmine Tags ([redmine_tags](https://github.com/ixti/redmine_tags))
* Redmine Tweaks ([redmine_tweaks](https://github.com/alexandermeindl/redmine_tweaks))
* Redmine Zen Edit ([redmine_zenedit](https://github.com/RCRM/redmine_zenedit))
* Hide Sidebar ([sidebar_hide](https://github.com/bdemirkir/sidebar_hide))
* Unread issues ([unread_issues](https://github.com/redcloak/unread_issues))

### 1.3 Available Themes

See [theme.ini](https://github.com/cytopia/redmine-like-a-boss/blob/master/redmine-themes/theme.ini) for description, license, author and version information.

* A1 Theme ([a1](https://github.com/RCRM/a1))
* Circle Theme ([circle](https://github.com/RCRM/circle))
* Coffee Theme ([coffee](https://github.com/RCRM/coffee))
* Redmine Gitmike Theme ([redmine-theme-gitmike](https://github.com/makotokw/redmine-theme-gitmike))
* Highrise Theme ([highrise](https://github.com/RCRM/highrise))
* Progressive Redmine Theme ([redmine-progressive-theme](https://github.com/stgeneral/redmine-progressive-theme))
* Redmine CRM Theme ([redminecrm](https://github.com/RCRM/redminecrm))

## 2. Usage

Simply start [redmine-like-a-boss.sh](https://github.com/cytopia/redmine-like-a-boss/blob/master/redmine-like-a-boss.sh) and follow the menu structure. No action will be taken without your explicit OK.

What actions does the script do?

* bundle update
* bundle install --without development test
* Database up/down migrations
* Build actions

The last two actions are defined in [plugin.ini](https://github.com/cytopia/redmine-like-a-boss/blob/master/redmine-plugins/plugin.ini) for each plugin separately.


### 2.1 Main Menu
```shell
------------------------------------------------------------
-                  Redmine like a boss                     -
------------------------------------------------------------

What do you want to do?

   2. List/check plugins
   3. Enable plugin
   4. Disable plugin

   5. List/check themes
   6. Enable theme
   7. Disable theme

   9. Exit program

Enter a number between 1-9: 2
```
### 2.2 List menu
```shell
------------------------------------------------------------
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

### 2.3 Enable menu
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

### 2.4 Disable menu
```shell
------------------------------------------------------------
-                  Redmine like a boss                     -
------------------------------------------------------------

Uninstall plugins

 1 Issuefy (0.2.0)
 2 Line numbers (1.0.0)

Enter the number of plugin to enable or 'q' to abort: 1
Uninstall "Issuefy" (issuefy) ? (Y/n)y
"Issuefy" does not require a database downgrade.
Remove symlink? (Y/n)y

"Issuefy" uninstalled. Restart Redmine

Press any key to continue...
```

## 3. Contribution

Feel free to add more plugins.
