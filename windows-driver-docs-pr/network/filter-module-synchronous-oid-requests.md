---
title: Filter Module Synchronous OID Requests
description: This topic describes Filter Module Synchronous OID requests
ms.assetid: 14C6555D-D8E6-4DEB-96C8-D4F18F06CE6B
keywords: Filter Module Synchronous OID Requests Interface, Filter Module Synchronous OID call, WDK Filter Module Synchronous OIDs, Filter Module Synchronous OID request
ms.date: 04/03/2017
ms.localizationpriority: medium
---

# Filter Module Synchronous OID Requests

To support the Synchronous OID request path, filter drivers provide a [*FilterSynchronousOidRequest*](https://docs.microsoft.com/windows-hardware/drivers/ddi/content/ndis/nf-ndis-filter_synchronous_oid_request) function entry point in the [**NDIS\_FILTER\_DRIVER\_CHARACTERISTICS**](https://docs.microsoft.com/windows-hardware/drivers/ddi/content/ndis/ns-ndis-_ndis_filter_driver_characteristics) structure when they call the [**NdisFRegisterFilterDriver**](https://docs.microsoft.com/windows-hardware/drivers/ddi/content/ndis/nf-ndis-ndisfregisterfilterdriver) function.

> [!NOTE]
> NDIS 6.81 supports specific OIDs for use with the Synchronous OID request interface. OIDs that existed before NDIS 6.80 and some NDIS 6.80 OIDs are not supported. To determine if an OID can be used in the Synchronous OID request interface, see the OID reference page.

To support the Synchronous OID request interface, use the documentation for the standard OID request interface. The following table shows the relationship between the functions in the Synchronous OID request interface and the standard OID request interface.

| Synchronous OID function | Standard OID function |
| --- | --- |
| [*FilterSynchronousOidRequest*](https://docs.microsoft.com/windows-hardware/drivers/ddi/content/ndis/nf-ndis-filter_synchronous_oid_request) | [*FilterOidRequest*](https://docs.microsoft.com/windows-hardware/drivers/ddi/content/ndis/nc-ndis-filter_oid_request) |
| [*FilterSynchronousOidRequestComplete*](https://docs.microsoft.com/windows-hardware/drivers/ddi/content/ndis/nf-ndis-filter_synchronous_oid_request_complete) | [*FilterOidRequestComplete*](https://docs.microsoft.com/windows-hardware/drivers/ddi/content/ndis/nc-ndis-filter_oid_request_complete) | 