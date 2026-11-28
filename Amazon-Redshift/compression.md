Redshift uses multiple compression techniques to achieve significant compression relational data stores.

Similar data is stored sequentially on disk

Does not require indexes or materialized views, which saves a lot of space compared to traditional systems

When loading data to an empty table, data is sampled and the most appropriate compression scheme is selected automatically