=== "🔎 Preview"

    ![ska-traffic-original.png is the image](assets/ska-traffic-original.png)

    [🛒 BUY](https://ska-webstore.tebex.io/category/standalone){ .md-button .md-button--primary }
    [🎬 Preview](https://www.youtube.com/watch?v=S4Z942uoA0Q){ .md-button .md-button--primary }

=== "🛠️​ Installation"

    #
    # Installation

    1. Add this resource into your `resources/` folder.

        Place the resource folder inside your server’s:
        ```
        resources/
        ```
        Example:
        ```
        resources/[ska]/ska-traffic
        ```

    2. Ensure it in your `server.cfg`.

        Add the following line to your server.cfg:
        ```
        ensure ska-traffic
        ```
        or:
        ```
        ensure [ska]
        ```
        
    3. Adjust any required configuration inside `shared/config.lua`.

    4. Restart Your Server

    No additional dependencies required.

    !!! info
        - Changes apply dynamically while players are connected
        - Works with all frameworks

=== "📜LICENSE"
    #
    END USER LICENSE AGREEMENT (EULA)

    Last updated: 2026

    Author / Licensor: SKA

    #
    1. DEFINITIONS

        “Software” refers to the FiveM script and all associated files, code, assets, and documentation provided by the Licensor.

        “Licensor” refers to SKA, the creator and owner of the Software.

        “Licensee” refers to the individual or entity that has purchased or obtained the Software through Tebex.

        “Server” refers to a FiveM server operated by the Licensee.

    2. LICENSE GRANT

        The Licensor grants the Licensee a limited, non-exclusive, non-transferable, non-sublicensable license to use the Software on their server(s), subject to the terms of this Agreement.

        This license grants usage rights only. No ownership, copyright, or intellectual property rights are transferred.

    3. COMMERCIAL USAGE

        the Licensee are expressly permitted to use the Software on commercial servers, including servers that:

        - Accept donations Sell in-game items, subscriptions, or perks 
        - Generate revenue through Tebex or similar platforms 

        This permission does not extend to: 
        
        - Reselling the Software Bundling the Software with other paid products 
        - Offering the Software as a service to third parties

    4. MODIFICATIONS

        the Licensee may modify configuration files explicitly provided by the Licensor for customization

        the Licensee may not Modify protected core files De-obfuscate or alter protected logic

        Unauthorized modification voids this license

    5. RESTRICTIONS

        the Licensee may not:

        - Redistribute, resell, sublicense, rent, lease, or share the Software in any form
        - Re-upload the Software publicly or privately
        - Share, leak, or publish the Software or any portion thereof Provide access to the Software to any third party 
        - Reverse engineer, decompile, disassemble, or attempt to bypass escrow, encryption, or obfuscation 
        - Include the Software in any bundle or package
        - Remove or alter copyright, branding, or license notices 
        - Claim authorship or ownership of the Software

        Any form of redistribution, whether free or paid, is strictly prohibited.

    6. OWNERSHIP

        The Software is and shall remain the exclusive property of the Licensor
        
        This Agreement does not convey any ownership rights or intellectual property interests
        
        All rights, title, and interest in and to the Software remain the exclusive property of the Licensor.

    7. UPDATES & SUPPORT

        Updates, patches, and bug fixes may be provided at the discretion of the Licensor 
        
        Support is provided only to verified purchasers 
        
        Major updates or feature expansions may require a separate purchase

    8. TERMINATION

        This license is automatically terminated if the Licensee violates any term of this Agreement.

        Upon termination, the Licensee must:

        - Stop using the Software
        - Delete all copies of the Software in their possession
        - No refund will be issued in the event of termination due to violation.

    9. DISCLAIMER OF WARRANTIES

        The Software is provided “AS IS”, without warranty of any kind, including but not limited to:

        - Fitness for a particular purpose
        - Compatibility with future FiveM updates
        - Error-free operation
        
        the Licensor does not guarantee uninterrupted operation or compatibility with third-party resources.

    10. LIMITATION OF LIABILITY

        To the maximum extent permitted by law, the Licensor shall not be liable for:

        - Any damages arising from the use or inability to use the Software
        - Loss of data, revenue, or server availability
        - Server crashes, conflicts, or misconfiguration
        - Use of the Software is entirely at the Licensee’s own risk.

    11. DMCA & COPYRIGHT ENFORCEMENT

        The Software is protected under international copyright law. 
        
        Unauthorized redistribution, resale, or leakage of the Software constitutes copyright infringement and may result in: 
        
        - Immediate license termination 
        - DMCA takedown notices 
        - Tebex enforcement actions
        - Permanent blacklist from the Licensor products 
        - Further Legal action where applicable

        The Licensor actively monitors and enforces its intellectual property rights.

    12. GOVERNING LAW

        This Agreement shall be governed by and interpreted in accordance with applicable laws, without regard to conflict of law principles.

    13. ACCEPTANCE

        By purchasing, downloading, installing, or using the Software, the Licensee acknowledges that they have read, understood, and agreed to the terms of this End User License Agreement.

    14. ENTIRE AGREEMENT

        This Agreement constitutes the entire agreement between the parties regarding the Software and supersedes all prior agreements, communications, or understandings, whether written or oral.

    #
    © 2026 SKA. All rights reserved.

=== "⚙️Configuration"
    #

    ```lua title="Config.lua"
    Config = {}

    -- Density (0.0 to 1.0)
    Config.pedFrequency = 0.0
    Config.trafficFrequency = 0.0

    -- 0.0 → No traffic / no peds
    -- 0.1 – 0.5 → Reduced traffic / peds
    -- 1.0 → Default GTA behavior


    -- Global Behavior Flags
    Config.DisablePolice = true
    Config.DisableAmbulance = true
    Config.DisableFiretrucks = true


    -- Driving Behavior
    Config.CruiseSpeed = 25.0 -- Speed in m/s
    Config.DrivingStyle = 786603

    -- 786603       Normal (Default)    Stops for lights, stays in lane, slows for turns, and avoids crashes. Very "legal."
    -- 1074528293   Rushed              Will weave through traffic and overtake slow cars, but usually tries to avoid head-on crashes.
    -- 2883621      Ignore Lights       Drives normally but completely ignores red lights and stop signs.
    -- 6            Very Strict         Will not even overtake a parked car. It will wait forever if the path is blocked.
    -- 524419       Semi-Aggressive     Good for "fast" traffic that still respects most rules but drives with urgency.
    -- 16777216     Emergency           The style used by Police/Ambulance. They drive through anything to reach their goal.
    ```