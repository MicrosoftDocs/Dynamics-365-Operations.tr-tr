---
title: Sabit kıymet alım deftere nakil hesapları
description: Bu makalede, genel muhasebe deftere nakil hesaplarının, kıymet alımları için nasıl ayarlanacağı açıklanmaktadır.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a3ac1580e33197c0cd8a82f34804d4639945d861
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "325377"
---
# <a name="fixed-asset-acquisition-posting-accounts"></a><span data-ttu-id="0a120-103">Sabit kıymet alım deftere nakil hesapları</span><span class="sxs-lookup"><span data-stu-id="0a120-103">Fixed asset acquisition posting accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a120-104">Bu makalede, genel muhasebe deftere nakil hesaplarının, kıymet alımları için nasıl ayarlanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="0a120-104">This article explains how to set up general ledger posting accounts for acquiring assets.</span></span>

<span data-ttu-id="0a120-105">Sabit kıymet alımlarını deftere nakletmek için kullanılan hesaplar kıymeti almak için kullanılan yönteme bağlı olarak değişebilir.</span><span class="sxs-lookup"><span data-stu-id="0a120-105">Accounts used for posting fixed asset acquisitions may vary depending upon the method used to acquire the asset.</span></span> <span data-ttu-id="0a120-106">Sabit kıymet nakil profilleri sayfasında, genel muhasebe hesapları sekmesinde, genel muhasebeye nakletmek için sabit kıymet hesaplarını ayarlamak için Alım ve Alım ayarlamayı seçin.</span><span class="sxs-lookup"><span data-stu-id="0a120-106">On the Fixed asset posting profiles page, on the Ledger accounts tab, select Acquisition and Acquisition adjustment to set up fixed asset accounts to post to the ledger.</span></span> 

<span data-ttu-id="0a120-107">Günlüklerde ve satınalma siparişlerinde, Genel muhasebe hesabı genellikle yeni bir sabit kıymetin alım değerinin borç kaydedildiği bilanço hesabıdır.</span><span class="sxs-lookup"><span data-stu-id="0a120-107">In journals and on purchase orders, Ledger account is typically the balance sheet account, where the acquisition value of the new fixed asset is debited.</span></span> <span data-ttu-id="0a120-108">Bu hesap günlüklerde görüntülenmez ve hareketlerde değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="0a120-108">This account is not displayed in the journal and cannot be replaced in transactions.</span></span> 

<span data-ttu-id="0a120-109">Mahsup hesap ayrıca bir bilanço hesabıdır.</span><span class="sxs-lookup"><span data-stu-id="0a120-109">Offset account is also a balance sheet account.</span></span> <span data-ttu-id="0a120-110">Genel günlükte ve sabit kıymetler günlüğünde, bu hesap genellikle kıymetin alımı için ödeme yapmak üzere kullanılan banka hesabı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="0a120-110">In the general journal and in the fixed assets journal, this account often will be the bank account that is used to pay for the acquisition of the asset.</span></span> <span data-ttu-id="0a120-111">Mahsup hesabı, günlüklerde tavsiye edilen bir varsayılan hesaptır.</span><span class="sxs-lookup"><span data-stu-id="0a120-111">The offset account is a default account, which is suggested in the journals.</span></span> <span data-ttu-id="0a120-112">Sabit kıymet bir satıcından satınalınmışsa, günlükte hesap planından bir diğer hesaba veya bir satıcı hesabına değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="0a120-112">It can be changed in the journal to any other account from the chart of accounts or to a vendor account, if the fixed asset was purchase from a vendor.</span></span> 

<span data-ttu-id="0a120-113">Borç hesaplarındaki fatura günlüğü veya Satınalma siparişleri sabit kıymet alımları için kullanılıyorsa, sabit kıymet hareketi için mahsup hesabı hareket için seçilen satıcı hesabı ile değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="0a120-113">When Invoice journal or Purchase orders in Accounts payable are used for fixed asset acquisitions, the offset account for the fixed asset transaction is replaced by the vendor account that is selected for the transaction.</span></span>

<span data-ttu-id="0a120-114">Genel muhasebedeki Stoktan sabit kıymetlere günlüğünü kullanarak nakledilmiş alımlar için, sabit kıymet harici kaynaklardan alınmaz ve şirketin kendi stokundan transfer edilir.</span><span class="sxs-lookup"><span data-stu-id="0a120-114">For acquisitions posted using the Inventory to fixed assets journal in General ledger, the fixed asset is not bought from external sources, but transferred from the company's own inventory.</span></span> <span data-ttu-id="0a120-115">Bu yüzden Stok yönetimindeki mahsup hesap, Stok yönetimindeki stok maddesi için bir stok çıkış hesabıdır.</span><span class="sxs-lookup"><span data-stu-id="0a120-115">Therefore, the offset account is an inventory issue account for the inventory item in Inventory management.</span></span>

<span data-ttu-id="0a120-116">Daha fazla bilgi için bkz: [Satınalma aracılığıyla kıymet alma](acquire-assets-procurement.md).</span><span class="sxs-lookup"><span data-stu-id="0a120-116">For more information, see [Acquire assets through procurement](acquire-assets-procurement.md).</span></span>



