=== "🔎 Preview"

    ![ska-solar-original.png is the image](assets/ska-solar-original.png)

    [🛒 BUY](https://ska-webstore.tebex.io/category/qbox){ .md-button .md-button--primary }
    [🎬 Preview](https://www.youtube.com/watch?v=wU8RPLMW5e0){ .md-button .md-button--primary }

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
        resources/[ska]/ska-solar
        ```

    2. Ensure it in your `server.cfg`.

        Add the following line to your server.cfg:
        ```
        ensure ska-solar
        ```
        or:
        ```
        ensure [ska]
        ```

    3. Adjust any required configuration inside `shared/config.lua`.

    4. add the lines below depending your inventory system

        === "qb-inventory"
            ```lua title="qb/qb-core/shared/items.lua"
            ska_tablet = { name = 'ska_tablet', label = 'Watt-A-Clean Tablet', weight = 2000, type = 'item', image = 'tablet.png', unique = false, useable = false, shouldClose = true, description = 'Expensive tablet' },
            ```

        === "ox_invertory"

            ```lua title="ox_inventory\data\items.lua"
            ['ska_tablet'] = {
                label = 'Watt-A-Clean Tablet',
                weight = 2000,
                stack = true,
                close = true,
                description = 'Expensive tablet',
                client = {
                    export = 'ska-tablet.openTablet'
                }
            },
            ```

    5. Restart Your Server

    # Dependencies

    * QBCore or ESX or QBOX Framework
    * Framework :
        - QBCORE  : (`qb-target` and `qb-inventory`) or (`ox_target` and `ox_lib` and `qb-inventory`)
        - QBOX    : `ox_target` and `ox_lib` and `ox_inventory`
        - ESX     : `ox_target` and `ox_lib` and `ox_inventory`
    * NUI support enabled

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

    7. SOURCE CODE & ESCROW

        The Software is distributed exclusively via Tebex Escrow.
        
        Source code is not provided The Software may be compiled, obfuscated, or otherwise protected 
        
        Any attempt to extract or reconstruct source code is strictly prohibited

    8. UPDATES & SUPPORT

        Updates, patches, and bug fixes may be provided at the discretion of the Licensor 
        
        Support is provided only to verified purchasers 
        
        Major updates or feature expansions may require a separate purchase

    9. NO REFUNDS

        This Software is a digital product. 
        
        All sales are final and non-refundable.

    10. TERMINATION

        This license is automatically terminated if the Licensee violates any term of this Agreement.

        Upon termination, the Licensee must:

        - Stop using the Software
        - Delete all copies of the Software in their possession
        - No refund will be issued in the event of termination due to violation.

    11. DISCLAIMER OF WARRANTIES

        The Software is provided “AS IS”, without warranty of any kind, including but not limited to:

        - Fitness for a particular purpose
        - Compatibility with future FiveM updates
        - Error-free operation
        
        the Licensor does not guarantee uninterrupted operation or compatibility with third-party resources.

    12. LIMITATION OF LIABILITY

        To the maximum extent permitted by law, the Licensor shall not be liable for:

        - Any damages arising from the use or inability to use the Software
        - Loss of data, revenue, or server availability
        - Server crashes, conflicts, or misconfiguration
        - Use of the Software is entirely at the Licensee’s own risk.

    13. DMCA & COPYRIGHT ENFORCEMENT

        The Software is protected under international copyright law. 
        
        Unauthorized redistribution, resale, or leakage of the Software constitutes copyright infringement and may result in: 
        
        - Immediate license termination 
        - DMCA takedown notices 
        - Tebex enforcement actions
        - Permanent blacklist from the Licensor products 
        - Further Legal action where applicable

        The Licensor actively monitors and enforces its intellectual property rights.

    14. GOVERNING LAW

        This Agreement shall be governed by and interpreted in accordance with applicable laws, without regard to conflict of law principles.

    15. ACCEPTANCE

        By purchasing, downloading, installing, or using the Software, the Licensee acknowledges that they have read, understood, and agreed to the terms of this End User License Agreement.

    16. ENTIRE AGREEMENT

        This Agreement constitutes the entire agreement between the parties regarding the Software and supersedes all prior agreements, communications, or understandings, whether written or oral.

    #
    © 2026 SKA. All rights reserved.

=== "⚙️Configuration"
    #
    ```lua title="Config.lua"
    Config = {}
    Config.Locale = 'en'

    -- NPC settings
    Config.JobPed = {
        model = "s_m_y_construct_01",
        coords = vector4(-701.08, 267.62, 83.15, 343.52),
        blip = {
            enabled = true,
            label = "Watt-A-Clean",
            sprite = 894,
            color = 46,
            scale = 0.8,
        }
    }

    -- Job vehicle
    Config.JobVehicle = "sadler"
    Config.VehicleSpawnPoints = {
        vector4(-745.93, 373.66, 87.87, 180.26),
        vector4(-749.43, 373.71, 87.87, 180.26),
        vector4(-752.93, 373.71, 87.87, 180.26),
        vector4(-756.43, 373.71, 87.87, 180.26),
        vector4(-759.63, 373.71, 87.87, 180.26),

    }

    -- Roof job locations
    Config.Contracts = {
        {
            id = 1,
            name = "Carcer WAY",
            house = vector3(-217.74, -229.34, 50.35),
            roofPoints = {
                vector4(-192.96, -225.57, 77.1, 340.0),
                vector4(-198.0, -240.7, 77.1, 340.0),
                vector4(-203.0, -255.7, 77.1, 340.0),
            },
            level = 1,
            reward = 100,
            solrep = 10,
            total = 3,
            exp = 0,
            dirt = 12,
        },
        {
            id = 2,
            name = "Red Desert AVE",
            house = vector3(-1294.14, -586.49, 29.3),
            roofPoints = {
                vector4(-1300.16, -569.9, 43.3, 311.0),
                vector4(-1296.8, -573.71, 43.3, 311.0),
                vector4(-1293.4, -577.57, 43.3, 311.0),
            },
            level = 1,
            reward = 100,
            solrep = 10,
            total = 3,
            exp = 0,
            dirt = 12,
        },
        {
            id = 3,
            name = "Vespucci BLVD",
            house = vector3(-584.64, -812.62, 26.33),
            roofPoints = {
                vector4(-521.85, -812.0, 45.20, 0.0),
                vector4(-521.88, -808.0, 45.20, 0.0),
                vector4(-574.88, -812.0, 45.20, 0.0),
                vector4(-574.88, -808.0, 45.20, 0.0),
                vector4(-580.88, -812.0, 45.20, 0.0),
                vector4(-580.88, -808.0, 45.20, 0.0),
            },
            level = 2,
            reward = 150,
            solrep = 15,
            total = 6,
            exp = 200,
            dirt = 16,
        },
        {
            id = 4,
            name = "Strawberry AVE",
            house = vector3(289.27, -994.9, 29.29),
            roofPoints = {
                vector4(294.0, -971.8, 43.75, 182.0),
                vector4(289.14, -971.95, 43.75, 182.0),
                vector4(289.08, -976.35, 43.75, 182.0),
                vector4(294.26, -976.2, 43.75, 182.0),
                vector4(262.42, -1022.84, 60.37, 160.0),
                vector4(264.27, -1018.0, 60.37, 160.0),
                vector4(266.07, -1013.01, 60.37, 160.0),
                vector4(268.07, -1008.01, 60.37, 160.0),

            },
            level = 2,
            reward = 150,
            solrep = 15,
            total = 8,
            exp = 200,
            dirt = 16,
        },
        {
            id = 5,
            name = "Vitus ST",
            house = vector3(-1318.8, -1266.91, 4.58),
            roofPoints = {
                vector4(-1330.58, -1275.13, 11.25, 290.0),
                vector4(-1332.56, -1270.05, 11.25, 290.0),
                vector4(-1334.43, -1264.97, 11.25, 290.0),
                vector4(-1336.33, -1259.79, 11.25, 290.0),
                vector4(-1331.06, -1257.96, 11.25, 290.0),
                vector4(-1329.23, -1263.06, 11.25, 290.0),
                vector4(-1327.38, -1268.16, 11.25, 290.0),
                vector4(-1325.5, -1273.42, 11.25, 290.0),
            },
            level = 3,
            reward = 200,
            solrep = 20,
            total = 8,
            exp = 350,
            dirt = 20,
        },
        {
            id = 6,
            name = "Popular ST",
            house = vector3(898.07, -875.5, 26.11),
            roofPoints = {
                vector4(903.39, -886.47, 40.5, 270.0),
                vector4(903.41, -891.42, 40.5, 270.0),
                vector4(903.38, -896.34, 40.52, 270.0),
                vector4(903.37, -901.36, 40.52, 270.0),
                vector4(908.38, -886.47, 40.5, 270.0),
                vector4(908.41, -891.42, 40.5, 270.0),
                vector4(908.38, -896.34, 40.52, 270.0),
                vector4(908.34, -901.31, 40.52, 270.0),
            },
            level = 3,
            reward = 200,
            solrep = 20,
            total = 8,
            exp = 350,
            dirt = 20,
        },
        {
            id = 7,
            name = "Senora FWY",
            house = vector3(2675.48, 3467.33, 55.59),
            roofPoints = {
                vector4(2698.0, 3518.98, 60.28, 247.0),
                vector4(2696.0, 3514.53, 60.28, 247.0),
                vector4(2694.0, 3510.07, 60.28, 247.0),
                vector4(2692.0, 3505.48, 60.28, 247.0),
                vector4(2690.0, 3500.93, 60.28, 247.0),
                vector4(2688.0, 3496.45, 60.28, 247.0),
                vector4(2686.0, 3492.01, 60.28, 247.0),
                vector4(2684.0, 3487.32, 60.28, 247.0),
                vector4(2682.0, 3482.48, 60.28, 247.0),
            },
            level = 4,
            reward = 250,
            solrep = 25,
            total = 9,
            exp = 600,
            dirt = 24,
        },
        {
            id = 8,
            name = "Orchardville AVE",
            house = vector3(977.24, -1979.97, 30.66),
            roofPoints = {


                vector4(959.0, -1988.0, 36.9, 265.0),
                vector4(958.6, -1993.0, 36.9, 265.0),
                vector4(958.2, -1998.0, 36.9, 265.0),
                vector4(957.8, -2003.0, 36.9, 265.0),
                vector4(957.4, -2008.0, 36.9, 265.0),


                vector4(955.0, -1988.0, 36.9, 265.0),
                vector4(954.6, -1993.0, 36.9, 265.0),
                vector4(954.2, -1998.0, 36.9, 265.0),
                vector4(953.8, -2003.0, 36.9, 265.0),
                vector4(953.4, -2008.0, 36.9, 265.0),

            },
            level = 4,
            reward = 250,
            solrep = 25,
            total = 10,
            exp = 900,
            dirt = 24,
        },
        {
            id = 9,
            name = "Paleto BLVD",
            house = vector3(-287.34, 6176.65, 31.5),
            roofPoints = {
                vector4(-313.15, 6195.75, 36.04, 135.0),
                vector4(-309.09, 6191.56, 36.04, 135.0),
                vector4(-304.72, 6187.28, 36.06, 135.0),
                vector4(-300.46, 6183.02, 36.06, 135.0),
                vector4(-296.29, 6178.78, 36.06, 135.0),
                vector4(-292.05, 6174.58, 36.06, 135.0),
                vector4(-287.8, 6170.36, 36.06, 135.0),
                vector4(-310.13, 6184.68, 36.06, 135.0),
                vector4(-305.74, 6180.36, 36.06, 135.0),
                vector4(-301.42, 6176.13, 36.06, 135.0),
                vector4(-297.23, 6171.95, 36.06, 135.0),
            },
            level = 5,
            reward = 300,
            solrep = 30,
            total = 11,
            exp = 600,
            dirt = 30,
        },
        {
            id = 10,
            name = "Great Ocean HWY",
            house = vector3(72.15, 6315.48, 31.23),
            roofPoints = {
                vector4(52.5, 6318.05, 37.62, 210.0),
                vector4(45.52, 6314.08, 37.62, 210.0),
                vector4(38.69, 6310.12, 37.62, 210.0),
                vector4(31.7, 6306.18, 37.62, 210.0),
                vector4(24.84, 6302.06, 37.62, 210.0),
                vector4(18.02, 6298.16, 37.62, 210.0),
                vector4(11.23, 6294.24, 37.62, 210.0),
                vector4(4.33, 6290.21, 37.62, 210.0),
                vector4(1.3, 6295.38, 37.62, 210.0),
                vector4(8.3, 6299.38, 37.62, 210.0),
                vector4(15.3, 6303.38, 37.62, 210.0),
                vector4(22.3, 6307.38, 37.62, 210.0),
                vector4(29.3, 6311.38, 37.62, 210.0),
                vector4(36.3, 6315.38, 37.62, 210.0),
                vector4(43.3, 6319.38, 37.62, 210.0),
                vector4(50.3, 6323.38, 37.62, 210.0),
            },
            level = 5,
            reward = 300,
            solrep = 30,
            total = 16,
            exp = 900,
            dirt = 30,
        },
        {
            id = 11,
            name = "South Rockford DR",
            house = vector3(-1428.13, -243.04, 46.38),
            roofPoints = {
                vector4(-1412.72, -240.32, 57.75, 312.0),
                vector4(-1416.72, -235.32, 57.75, 312.0),
                vector4(-1410.72, -235.32, 57.75, 312.0),
                vector4(-1404.72, -235.32, 57.75, 312.0),
                vector4(-1438.72, -230.32, 57.75, 312.0),
                vector4(-1432.72, -230.32, 57.75, 312.0),
                vector4(-1420.72, -230.32, 57.75, 312.0),
                vector4(-1414.72, -230.32, 57.75, 312.0),
                vector4(-1408.72, -230.32, 57.75, 312.0),
                vector4(-1402.72, -230.32, 57.75, 312.0),
                vector4(-1442.72, -225.32, 57.75, 312.0),
                vector4(-1436.72, -225.32, 57.75, 312.0),
                vector4(-1430.72, -225.32, 57.75, 312.0),
                vector4(-1424.72, -225.32, 57.75, 312.0),
                vector4(-1418.72, -225.32, 57.75, 312.0),
                vector4(-1412.72, -225.32, 57.75, 312.0),
                vector4(-1406.72, -225.32, 57.75, 312.0),
                vector4(-1438.72, -220.32, 57.75, 312.0),
                vector4(-1432.72, -220.32, 57.75, 312.0),
                vector4(-1408.72, -220.32, 57.75, 312.0),
            },
            level = 6,
            reward = 350,
            solrep = 35,
            total = 20,
            exp = 1300,
            dirt = 35,
        },
        {
            id = 12,
            name = "Hangar WAY",
            house = vector3(811.48, -2504.98, 28.37),
            roofPoints = {
                vector4(842.44, -2518.0, 39.3, 355.0),
                vector4(847.44, -2518.4, 39.3, 355.0),
                vector4(852.44, -2518.8, 39.3, 355.0),
                vector4(842.44, -2522.0, 39.3, 355.0),
                vector4(847.44, -2522.4, 39.3, 355.0),
                vector4(852.44, -2522.8, 39.3, 355.0),
                vector4(842.44, -2526.0, 39.3, 355.0),
                vector4(847.44, -2526.4, 39.3, 355.0),
                vector4(852.44, -2526.8, 39.3, 355.0),
                vector4(872.42, -2523.0, 47.1, 355.0),
                vector4(877.42, -2523.4, 47.1, 355.0),
                vector4(882.42, -2523.8, 47.1, 355.0),
                vector4(872.42, -2528.0, 47.1, 355.0),
                vector4(877.42, -2528.4, 47.1, 355.0),
                vector4(882.42, -2528.8, 47.1, 355.0),
                vector4(872.42, -2533.0, 47.1, 355.0),
                vector4(877.42, -2533.4, 47.1, 355.0),
                vector4(882.42, -2533.8, 47.1, 355.0),
                vector4(817.0, -2512.84, 39.3, 355.0),
                vector4(816.6, -2517.84, 39.3, 355.0),
                vector4(816.2, -2522.84, 39.3, 355.0),
                vector4(815.8, -2527.84, 39.3, 355.0),
            },
            level = 6,
            reward = 350,
            solrep = 35,
            total = 22,
            exp = 1300,
            dirt = 35,
        },
    }

    -- Props
    Config.DirtyPanelProp = "ska_prop_dirtysolarpanel"
    Config.CleanPanelProp = "ska_prop_cleansolarpanel"

    -- Job outfit
    Config.JobOutfit = {
        male = {
            ["t-shirt"] = { item = 15, texture = 0 },
            ["torso2"] = { item = 43, texture = 0 },
            ["arms"] = { item = 145, texture = 5 },
            ["pants"] = { item = 47, texture = 0 },
            ["shoes"] = { item = 25, texture = 0 },
            ["hat"] = { item = 145, texture = 0 },
            ["glasses"] = { item = 9, texture = 0 }
        },
        female = {
            ["t-shirt"] = { item = 15, texture = 0 },
            ["torso2"] = { item = 86, texture = 0 },
            ["arms"] = { item = 171, texture = 5 },
            ["pants"] = { item = 49, texture = 0 },
            ["shoes"] = { item = 25, texture = 0 },
            ["hat"] = { item = 144, texture = 0 },
            ["glasses"] = { item = 10, texture = 2 }
        }
    }


    Config.COOLDOWN_DURATION = 1800 --sec
    Config.EXPIRY_DURATION = 1800 --sec
    Config.MAX_DISTANCE = 20
    ```