======================
Heroku
======================
Heroku is a Platform-as-a-Service (PaaS) solution that allows developers to host, manage, and scale applications in the cloud.
Heroku supports a variety of programming languages and provides an easy, fast, and reliable way to deploy applications without having to worry about infrastructure.

Open Heroku:

    1. Open your browser and go to:

    .. code-block:: console

        www.heroku.com

    2. Create an account or login to your account.
    3. The first site that you can see is a overview about your projects.
    4. Select your Novaland Project.

Your Project on Heroku
======================

Overview of your App:
______________________
The overview of a Heroku app shows the following information:

    - App name and its unique URL
    - Application status (running or crashed)
    - Dynos (number of web or worker processes running)
    - Add-ons (list of any installed add-ons)
    - Collaborators (list of people who have access to the app)
    - Last release (when the app was last updated and the status of the update)
    - Metrics (resource usage of the app, including memory, CPU, and bandwidth usage)

Open your project
________________________
Just click on the 'Open app' Button at the top right of the screen.

Ressources
======================

In the context of Heroku, resources refer to the various add-ons and services that you can use to extend the functionality of your application. Some of the common resources on Heroku include:

    1. Databases: Heroku provides several options for managed databases, including PostgreSQL, MySQL, and MongoDB.
    2. Analytics: You can use resources such as Heroku Metrics, Logs, and Monitoring to track the performance of your application and identify any issues.
    3. Email: You can use resources like SendGrid, Mandrill, and Mailgun to manage your email delivery needs.
    4. Storage: Heroku provides resources for file storage, including Amazon S3, Google Cloud Storage, and Dropbox.
    5. Security: You can use resources such as Okta, Auth0, and AWS Security to enhance the security of your application.

By adding these resources to your Heroku app, you can enhance the functionality and performance of your application, making it easier to manage and scale.

Add a ressource to your app
_______________________________

    1. To add an add-on, go to the "Resources" tab in your Heroku app dashboard and search for the add-on you want to use.
    2. Then, simply click on the add-on to add it to your app.

Heroku Postgres
===================
Postgres on Heroku is a managed database service provided by Heroku that enables you to run your PostgreSQL database in the cloud.
PostgreSQL is an open-source relational database management system, and the Postgres service on Heroku provides a fully managed, scalable, and secure database solution for applications hosted on the Heroku platform.

With Postgres on Heroku, you can easily manage and scale your database, ensuring that your application always has the necessary resources to handle high traffic and large amounts of data.
Additionally, Heroku provides several tools and services to monitor, backup, and recover your PostgreSQL database, making it a reliable and scalable option for your database needs.

Save the participants data
________________________________
If you have added Heroku Postgres as an add-on to your app, it will serve as the database for storing all the variables and functions associated with your oTree project.
The naming of these variables is determined within your PyCharm project or another development environment and cannot be altered in the Heroku Postgres database.

Download the participant information
__________________________________
You can download this list of variables and functions as a .CSV file for further analysis directly from the Heroku Dashboard.

    1. Go to the "Resources" tab in your app dashboard
    2. select the Heroku Postgres database
    3. click on the "Backups" section
    4. then, click on the "Download" button to download the latest backup as a .CSV file


Reset the Database
____________________________

Papertrail
==========================
Papertrail is a powerful log management solution that helps developers keep their applications running smoothly. With Papertrail's central log management, developers can easily find and fix issues without having to sift through multiple log sources.
With Papertrail, you can quickly and easily see all of your Heroku logs in one place.
No more logging into multiple systems just to find what you need - Papertrail has got you covered.

Here are just a few of the great features you'll get with Papertrail on Heroku:

    1. Centralized log management for all your Heroku apps
    2. Real-time log analysis and search
    3. Alerts for important events, so you can take action quickly
    4. Integration with multiple programming languages and frameworks
    5. Secure, scalable log storage that grows with your needs

Sentry
==========================
Sentry is an error tracking and monitoring software that helps developers identify and resolve issues in their applications.
Sentry integrates with various platforms, including Heroku, to provide real-time alerts, stack traces, and error details to developers, enabling them to quickly fix bugs and improve the performance of their applications.
By integrating Sentry with Heroku, developers can receive notifications about errors and performance issues that occur within their Heroku-hosted applications, allowing them to resolve issues before they affect users.

What features does Sentry offer on Heroku?

    1. Real-time error tracking
    2. Stack trace analysis
    3. Collaboration tools for development teams
    4. Customizable alerts and notifications
    5. Integration with various programming languages and frameworks