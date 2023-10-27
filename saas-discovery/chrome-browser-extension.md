# Chrome Browser Extension Installation Admin Guide

Once your Resmo admin triggers an email from the SaaS Directory UI, you will receive an email from Resmo. After clicking on the link provided in the email, the extension installation process will begin. Recipients proceed to the related page and install the extension for their browsers.&#x20;

Resmo then starts using the browser extension to capture employee SaaS logins and shows the collected data on the [Apps Dashboard](saas-discovery-apps-dashboard.md) and [Employees Dashboard](saas-discovery-employees-dashboard.md).

### Installing the browser extension

Go to the SaaS Discovery configuration screen and see the Browser Extensions section. There are three options to choose from:

* **Copy your installation link:** You can use this link to copy your unique installation link and test it before sending it out to everyone.
* **Send installation link to everyone:** Clicking this button triggers an email that will send the installation link to everyone in your directory integration. By clicking the provided link in the email, recipients can proceed with the installation process.

<figure><img src="../.gitbook/assets/resmo-browser-extension (1).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
You can add more than one browser or browser profile using your token. Once you have installed the extension, the setup process is complete.
{% endhint %}

This feature enables you to easily install the Resmo browser extension and begin monitoring your organization's SaaS activity. By adding multiple browsers or profiles, you can customize the monitoring to meet your organization's needs.

### Browser Extension MDM Installation Guide

You can install Resmo’s browser extension in your organization through several MDM (Mobile Device Management) solution to ensure seamless rollout. There are several ways to install.

#### Chrome Browser Management

1. In the Resmo go Settings and Browser Extension page, copy your organization token.
2. Navigate to the [Google Admin Console](https://admin.google.com/).
3. Sign in with your administrator account.
4. From the Devices section, select "Chrome."
5. On the Chrome management page, click on "Apps & extensions."
6. Click “Users & Browsers” tab.
7. On the right bottom of the page, click the yellow plus (+) button and select “Add Chrome app or Extension by ID”

<figure><img src="../.gitbook/assets/apps-and-extensions.png" alt=""><figcaption></figcaption></figure>

8. In the form, write Resmo’s extension ID, bbccnhenkklbacbmpfbjfpellahdfedp and save.
9. You’ll see the Resmo will be added to your list.&#x20;
10. Click on the Resmo logo on the list and in the Installation policy select. “Force Install + pin to browser toolbar”
11. In the Policy for extension write your organization token in the format: {"orgToken": {"Value": "YOUR TOKEN"\}}

<figure><img src="../.gitbook/assets/users-and-browsers.png" alt=""><figcaption></figcaption></figure>

This method is compatible with most of the MDM solutions for macOS. The following is the sample configuration. Remember to replace REPLACE\_ORG\_TOKEN with your organization token, which you can grab from Settings -> Browser Extension page. Bbccnhenkklbacbmpfbjfpellahdfedp is Resmo’s Chrome extension ID, which is hard codded.

## MDM Policy for macOS:

1. Click the Save button on the top.&#x20;
2. The extension will roll out to your users gradually and you’ll be able to collect.&#x20;

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
    <dict>
        <key>PayloadContent</key>
        <array>
            <dict>
                <key>PayloadContent</key>
                <dict>
                    <key>com.google.Chrome</key>
                    <dict>
                        <key>Forced</key>
                        <array>
                            <dict>
                                <key>mcx_preference_settings</key>
                                <dict>
                                    <key>ExtensionInstallForcelist</key>
                                    <array>
                                        <string>bbccnhenkklbacbmpfbjfpellahdfedp;https://clients2.google.com/service/update2/crx</string>
                                    </array>
                                </dict>
                            </dict>
                        </array>
                    </dict>
                </dict>
                <key>PayloadEnabled</key>
                <true/>
                <key>PayloadIdentifier</key>
                <string>com.resmo.chrome.bbccnhenkklbacbmpfbjfpellahdfedp</string>
                <key>PayloadType</key>
                <string>com.apple.ManagedClient.preferences</string>
                <key>PayloadUUID</key>
                <string>8A2E404C-D67E-4F93-BC04-529F939FABF8</string>
                <key>PayloadVersion</key>
                <integer>1</integer>
            </dict>
            <dict>
                <key>PayloadContent</key>
                <dict>
                    <key>com.google.Chrome.extensions.bbccnhenkklbacbmpfbjfpellahdfedp</key>
                    <dict>
                        <key>Forced</key>
                        <array>
                            <dict>
                                <key>mcx_preference_settings</key>
                                <dict>
                                    <key>orgToken</key>
                                    <string>REPLACE_ORG_TOKEN</string>
                                </dict>
                            </dict>
                        </array>
                    </dict>
                </dict>
                <key>PayloadEnabled</key>
                <true/>
                <key>PayloadIdentifier</key>
                <string>com.resmo.chrome.D658A52D-317C-4D10-A45E-D2CE72B33566</string>
                <key>PayloadType</key>
                <string>com.apple.ManagedClient.preferences</string>
                <key>PayloadUUID</key>
                <string>D658A52D-317C-4D10-A45E-D2CE72B33566</string>
                <key>PayloadVersion</key>
                <integer>1</integer>
            </dict>
        </array>
        <key>PayloadDescription</key>
        <string>Automatic enrollment for Resmo chrome extension</string>
        <key>PayloadDisplayName</key>
        <string>Resmo Chrome Extension</string>
        <key>PayloadIdentifier</key>
        <string>com.google.Chrome.extensions.bbccnhenkklbacbmpfbjfpellahdfedp</string>
        <key>PayloadOrganization</key>
        <string></string>
        <key>PayloadRemovalDisallowed</key>
        <true/>
        <key>PayloadScope</key>
        <string>System</string>
        <key>PayloadType</key>
        <string>Configuration</string>
        <key>PayloadUUID</key>
        <string>FEE7D91B-5977-4979-BD0C-E077484699F3</string>
        <key>PayloadVersion</key>
        <integer>1</integer>
    </dict>
</plist>
```

#### MDM Policy for Windows

Coming soon.
