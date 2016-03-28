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

## Contribution

Feel free to add more plugins.
