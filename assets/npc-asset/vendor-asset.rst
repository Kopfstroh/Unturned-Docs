.. _doc_npc_asset_vendor:

Vendor Assets
=============

**GUID** *32-digit hexadecimal*: Refer to :ref:`GUID <doc_data_guid>` documentation.

**Type** *enum* (``Vendor``)

**ID** *uint16*: Must be a unique identifier.

Buying
------

Properties pertaining to items that the vendor is willing to buy from players. Vendors can set conditions for the items they are buying. These conditions are prefixed with ``Buying_#_``. For example, ``Buying_0_Conditions 1``. For more information, refer to the documentation for :ref:`Conditions <doc_npc_asset_conditions>` and :ref:`Rewards <doc_npc_asset_rewards>` respectively.

**Buying** *byte*: Total number items being bought by the vendor.

**Buying\_#\_ID** *uint16*: ID of item to buy from the player.

**Buying\_#\_Cost** *uint32*: Amount of currency to pay the player. Defaults to experience points as the currency, unless the Currency property has been set.

Selling
-------

Properties pertaining to items or vehicles that the vendor is willing to sell to players. Vendors can set conditions for the items/vehicles they are selling. These conditions are prefixed with ``Selling_#_``. For example, ``Selling_0_Conditions 1``. For more information, refer to the documentation for :ref:`Conditions <doc_npc_asset_conditions>` and :ref:`Rewards <doc_npc_asset_rewards>` respectively.

**Selling** *byte*: Total number of items/vehicles being sold by the vendor.

**Selling\_#\_Type** *enum* (``Item``, ``Vehicle``): Type of asset being sold.

**Selling\_#\_ID** *uint16*: ID of item/vehicle to sell to the player.

**Selling\_#\_Cost** *uint32*: Amount of currency to pay the vendor. Defaults to experience points as the currency, unless the Currency property has been set.

**Selling\_#\_Spawnpoint** *string*: Location to spawn the purchased vehicle, using the spawnpoint name as set in the Devkit level editor. For example, ``Liberator_Jet``.

Other Properties
----------------

**Disable_Sorting** *flag*: Disable vendor sorting.

**Currency** *string*: GUID of the :ref:`currency asset <doc_assets_currency>` to use as currency instead of experience points.

**FaceOverride** *byte*: Optional index of face image to use when this vendor is opened. Face is reset to character's default when unspecified or when a new message is opened.

Localization
------------

**Name** *string*: Vendor name in user interfaces.

**Description** :ref:`doc_data_richtext`: Vendor description in user interfaces.
