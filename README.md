# WHMCS License Bypass with Updates (License.php)

I am pleased to share the result of my recent complete update project for the License.php file in WHMCS. Although it was a challenge, I enjoyed every moment dedicated to researching and simplifying the solution. Over the years, I have contributed significantly to this community, and despite my attempts to report this issue to WHMCS, the response was not positive. For this reason, I decided to share this solution with those who wish to use this incredible software for their projects

![Force Check](https://github.com/k4t3pr0/WHMCS-ByPass-License/blob/main/img/force_license.png?raw=true)

How does it work? Simply replace the License.php file in the location of your WHMCS installation, either before or after installing the software. The path is:

```
/vendor/whmcs/whmcs-foundation/lib/License.php
```
**This license file is designed for versions higher than v8.8.x.**

Feel free to enter any license number both during the initial installation and after installing it in the configuration.php file. Everything is verified with the License.php file.

I reiterate, with this solution, you can have a FULL WHMCS with all official WHMCS updates. (You can review the code; my approach was to maintain almost all original validations and adjust only what was necessary for the software to believe it has a valid license. However, all validations are performed with WHMCS servers.):

```
    const LICENSE_API_HOSTS = ["a.licensing.whmcs.com", "b.licensing.whmcs.com", "c.licensing.whmcs.com", "d.licensing.whmcs.com", "e.licensing.whmcs.com", "f.licensing.whmcs.com"];
    const STAGING_LICENSE_API_HOSTS = ["hou-1.licensing.web.staging.whmcs.com"];
```

When you finish installing your license file, you must force the update of your local license, to do this execute the red "force license update" button that appears in:

```
"whmcs_path/admin/help/license"
```
![Check Update](https://github.com/k4t3pr0/WHMCS-ByPass-License/blob/main/img/update_check.png?raw=true)