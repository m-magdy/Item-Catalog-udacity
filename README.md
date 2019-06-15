# Catalog App

## Description
This application provides a list of items within a variety of categories. 
The list of categories and items comes from [Facebook Pages for Marketing](https://www.facebook.com/business/products/pages). 
"Page type" (Local Business or Place, Company, Organization or Institution, ...) and "Category" from this Facebook page represents respectively "category" and "item" for this project.

A third party authentication system (Google and Facebook) is implemented to let users add, update and delete items. 

This app implements also API endpoints with responses formatted in JSON.


## Requirements

- [Vagrant](https://www.vagrantup.com/)
- [VirtualBox](https://www.virtualbox.org/)

We assume that [Flask](http://flask.pocoo.org), [SQLAlchemy](http://www.sqlalchemy.org), 
[SQLite](https://www.sqlite.org/) and [oauth2client](https://github.com/google/oauth2client) 
are already installed in the virtual machine (VM).


## Set Up

1. Clone the [fullstack-nanodegree-vm repository](https://github.com/udacity/fullstack-nanodegree-vm).

2. Look for the *catalog* folder and replace it with the contents of this respository.

## Usage

Launch the Vagrant VM from inside the *vagrant* folder with:

`vagrant up`

Then access the shell with:

`vagrant ssh`

Then Download or clone the [catalog-app](https://github.com/boisalai/catalog-app) repository under `/catalog` 
move this directory under your `/vagrant` directory (like that: `/vagrant/catalog`)

Create and populate the database.

```bash
$ python data.py
```

Run the application.

```bash
$ python application.py
```

Open your web browser to this URL: http://localhost:8000

## API endpoints

| Request | Methods | What you get | 
| ------------- |-------------|---------|
| /catalog.json | GET | All categories with their items. |
| /v1/categories | GET | All categories with their items. |
| /v1/categories/*category_name* | GET | A specific category with his items. |
| /v1/categories/*category_name*/*item_title* | GET | A specific item. |


