# What to do if you think your site has been hacked
If you've noticed any of the following, there's a good chance a malicious actor gained illegitimate access to your application and is currently abusing it:

- Your site now redirects to some shady, ad-filled other website
- You've noticed an admin user in your back-end you're pretty sure you didn't create
- You're receiving spam mails from your own contact form

Unfortunately, there's lots of other abuse that can be happening that won't be as visible, so this is not an exhaustive list.
## First response
Since these cases can have a large impact, doing the right things right away is essential to mitigating the consequences. So we've listed some first steps we recommend you take as soon as possible.
### Get your devs involved
No one will be better suited to figure out exactly where the vulnerability was and how it can be mitigated than your application's developers.
### Check the impact
Verify what might have been compromised. Check your application for illegitimate users, mail abuse, or dodgy redirects, to know what to check for after potential fixes were applied. Make note of this information to refer to later.
### Check your modules
Check your site's plugins/addons/modules for updates, in open source CMS web applications these are by far the biggest recurring vulnerability being exploited.
### Check your database
Critically assess whether your database needs restoring. It's understandable to not want to lose any data, but it's likely that the malicious actor had database access through the application, so user tables or other access-related tables might've been compromised.
### Check your credentials
Many CMSes have a file containing secrets that might be compromised. You can contact us to request a reset of the MySQL password, but you might also have API keys or 3rd party credentials that need rotating.
## Nuclear option: full reinstall
Partial fixes tend to leave backdoors or other malware, fully scrubbing your code and replacing it with a clean version, either from backup or source is preferrable. It's important to consider the database in this, since restoring that might be necessary if malicious users were added but you need to consider what data you might lose when restoring to the latest available datapoint and export it out of the application first.

The exact process for restoring your site from backup/source differs depending on its components. Generally, you follow this template:
!!!warning
This procedure includes destroying your data, so be sure you understand what you're doing before attempting this
!!!

- Delete the current files and database
- Rotate your credentials
- Reinstall the website from your clean source
- Make sure your codebase is up to date


