# Template Site

* This is just a simple template I've created after finding I use the same stuff in almost every Rails project. If there is a better way to do something here, please let me know!

* This has basic user authentication already. If you want to add or remove fields, start with the create_users migration in the /db/migrate directory. There are current_user and user_signed_in? methods similar to Devise. 

* This project uses Bootstrap, Bootswatch, Simple_Form, and HAML.

### Usage Instructions
1. Clone repo to your local computer
	*  git clone https://github.com/sean-perryman/TemplateSite.git /your/directory/here
2. Remove old git into
	* cd /your/cloned/repo/directory
	* rm -rf .git
3. Change DB info
	* Edit /config/database.yml
	* Change TemplateSite to reflect your application name
4. Migrate DB locally
	* rake db:create
	* rake db:migrate
5. Install Simple Form Bootstrap
	* rails g simple_form:install --bootstrap
6. Precompile assets (for Heroku)
	* rake assets:precompile
7. Initialize new git repo
	* git init
8. Make a inital commit
	* git add .
	*  git commit -m "Initial"
9. Create Heroku app
	* heroku create
10. Push to Heroku
	* git push heroku master
11. Migrate DB
	* heroku run rake db:migrate


### Subsequent Pushes to Heroku
1. Precompile assets
	* rake assets:precompile
2. Commit changes
	* git add --all .
	* git commit -m "Message goes here"
3. Push to Heroku
	*  git push heroku master
4. (Optional) Migrate DB on Heroku
	* heroku run rake db:migrate
