<h1>Master Data - for Managing about Clients</h1>

<p>You should create an adminpanel-like system to manage Clients, Projects, Tasks with CRUD operations.</p>

<p>A few screenshots from the example solutions:</p>

<p><img alt="CRM Demo 1" src="https://github.com/skputra-aol/Php-Laravel/blob/master/Data-Master-App/img/129160013-d5c895d3-92aa-4a32-9a62-d09807f623f9.png?raw=true" /></p>

<p><img alt="CRM Demo 2" src="https://github.com/skputra-aol/Php-Laravel/blob/master/Data-Master-App/img/129160023-8095c1b5-d6ce-4813-b708-af1b16605160.png?raw=true" /></p>

<p>You can come up with whatever structure of the database tables you want, but please try to use all the Laravel features listed below.</p>

<hr />
<h3>Features to implement</h3>

<p>Here&#39;s the <a href="https://laraveldaily.com/roadmap-learning-path">list of Roadmap features</a> you need to try to implement in your code:</p>

<p><strong>Create Routing Advanced</strong></p>

<ul>
	<li>Route Model Binding in Resource Controllers</li>
	<li>Route Redirect - homepage should automatically redirect to the login form</li>
</ul>

<p><strong>Database Advanced</strong></p>

<ul>
	<li>Database Seeders and Factories - to automatically create first clients/projects/tasks and default users</li>
	<li>Eloquent Query Scopes - show only active clients, for example</li>
	<li>Polymorphic relationships with <a href="https://github.com/spatie/laravel-medialibrary">Spatie Media Library package</a></li>
	<li>Eloquent Accessors and Mutators - view all date values in <code>m/d/Y</code> format</li>
	<li>Soft Deletes on any Eloquent models</li>
</ul>

<p><strong>Auth Advanced</strong></p>

<ul>
	<li>Authorization: Roles/Permissions (admin and simple users), Gates, Policies with <a href="https://github.com/spatie/laravel-permission">Spatie Permissions package</a></li>
	<li>Authentication: Email Verification</li>
</ul>

<p><strong>API Basics</strong></p>

<ul>
	<li>API Routes and Controllers</li>
	<li>API Eloquent Resources</li>
	<li>API Auth with Sanctum</li>
	<li>Override API Error Handling and Status Codes</li>
</ul>

<p><strong>Debugging Errors</strong></p>

<ul>
	<li>Try-Catch and Laravel Exceptions</li>
	<li>Customizing Error Pages</li>
</ul>

<p><strong>Sending Email</strong></p>

<ul>
	<li>Mailables and Mail Facade</li>
	<li>Notifications System: Email</li>
</ul>

<p><strong>Extra</strong></p>

<ul>
	<li>Automated Tests for CRUD Operations</li>
</ul>

<p>&nbsp;</p>

<p>&nbsp;</p>

<p>&nbsp;</p>

<h1>Support Ticket</h1>

<p>&nbsp;</p>

<h3>Quick description</h3>

<p>A system to manage support tickets. customers register as users and can create tickets, then admins assign them to agents, and all parties can view ticket statuses.</p>

<p>A few screenshots from the example solution:</p>

<p><img alt="Laravel support tickets 01" src="https://laraveldaily.com/uploads/2022/11/laravel-support-tickets-01.png" /></p>

<p><img alt="Laravel support tickets 02" src="https://laraveldaily.com/uploads/2022/11/laravel-support-tickets-02.png" /></p>

<hr />
<h3>Database structure</h3>

<p>Every ticket needs to have:</p>

<ul>
	<li>title (required)</li>
	<li>text description (required)</li>
	<li>multiple files attached (optional)</li>
	<li>priority (choose from a few options)</li>
	<li>status (choose from a few options like open/closed)</li>
	<li>assigned user agent (foreign key to users table)</li>
	<li>multiple categories (belongsToMany relationship with categories table)</li>
	<li>multiple labels (belongsToMany relationship with labels table)</li>
</ul>

<hr />
<h3>Auth</h3>

<p>There should be login and register functionality, they may come from starter kit like Laravel Breeze or other one of your choice.</p>

<p>Every user needs to have one of three roles:</p>

<ul>
	<li>Regular user (default)</li>
	<li>Agent</li>
	<li>Administrator</li>
</ul>

<p>New users can register and they are assigned Regular articles role.</p>

<p>There should be one Administration user created with database seeds.</p>

<p>After registration or login, users get inside the system which would look like a typical adminpanel to manage data: menus, tables, CRUDs for administrator.</p>

<hr />
<h3>Regular users: manage THEIR tickets</h3>

<p>After registration/login, user sees the only menu item &quot;Tickets&quot; with a table of tickets only created by themselves.</p>

<p>Table of tickets needs to have dropdown filters: by status, priority and category.</p>

<p>They can add a new ticket, but can&#39;t edit/delete tickets.</p>

<p>They can click the ticket title in the table to open the page to see more details and ticket activity log and comments, also may add a comment there (more on that later).</p>

<hr />
<h3>Agent users: manage THEIR tickets</h3>

<p>Similar to regular users, agents see only tickets, and only their tickets, but &quot;their&quot; has different meaning - not that they created the tickets, but are assigned to them (by admin, more on that later).</p>

<p>They can edit tickets and add comments.</p>

<hr />
<h3>Admin users: manage everything</h3>

<p>Admins see not only tickets table, but also can view more menu items:</p>

<ul>
	<li>Dashboard with the amount of tickets per status (total / open / closed, etc.)</li>
	<li>Manage Labels, Categories, Priorities and Users, in CRUD way</li>
</ul>

<p>Also, when editing the ticket, admins can assign Agent user to it - other users shouldn&#39;t see that field.</p>

<p>Also, admins should see the menu item called &quot;Logs&quot; which lists all changes that happened to all tickets, like history: who created/updated the ticket and when.</p>

<hr />
<h3>Ticket Comments</h3>

<p>After clicking on ticket, any user can get to its page, and there should be a form to add a comment, and that page shows the list of comments, like on a typical blogpost page.</p>

<hr />
<h3>Email Notifications</h3>

<p>When the new ticket is created, admin should get an email with the link to the Edit form of the ticket.</p>

<p>&nbsp;</p>

<p>&nbsp;</p>
