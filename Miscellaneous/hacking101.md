# What to do if you think your site has been hacked
If you've noticed any of the following, there's a good chance a malicious actor gained illegitimate access to your application and is currently abusing it:

- Your site now redirects to some shady, ad-filled other website
- You've noticed an admin user in your back-end you're pretty sure you didn't create
- You're receiving spam mails from your own contact form

Unfortunately, there's lots of other abuse that can be happening that won't be as visible, so this is not an exhaustive list.
## First response
Since these cases can have an incredibly large impact, doing the right things right away is essential to mitigating the consequences. So we've listed some first steps we recommend you take as soon as possible.
### Check the impact
Verify what might have been compromised. Check your application for illegitimate users, mail abuse, or dodgy redirects, to know what to check for after potential fixes were applied. Make note of this information to refer to later
### Nuclear option: full reinstall
Trying to fix the symptoms can take longer and has the potential to miss some backdoor malware, so the most secure and often fastest option is to restore the application, either from a backup before the infection or directly from your source code. It's important to consider the database in this, since restoring that might be necessary if malicious users were added but you need to consider what data you might lose when restoring to the latest available datapoint and export it out of the application first.

The exact process for restoring your site from backup/source differs depending on its components. Below is a sample process for a simple WordPress installation

1. 
------------------------
Recommendations:

0. Get your devs involved. No one will be better suited to figure out exactly where the vulnerability was and how it can be mitigated than your application's developers.
1. Partial fixes tend to leave backdoors or other malware, fully scrubbing your code and replacing it with a clean version, either from backup or source is preferrable
2. When reinstalling, make sure to check core code, plugins, modules, themes et al. for updates, in public CMS-based web applications these are by far the biggest recurring vulnerability being exploited
3. Critically assess whether your database needs restoring. It's understandable to not want to lose any data, but it's likely that the malicious actor had database access through the application, so user tables or other access-related tables might've been compromised. 
4.