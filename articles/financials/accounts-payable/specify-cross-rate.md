---
title: "Çapraz kuru belirtme"
description: "Bu konu, Microsoft Dynamics 365 for Finance and Operations'taki çapraz kurlar hakkında bilgi vermektedir."
author: abruer
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cf531c3a8f3bdb17314d1de436b98249169f82a3
ms.openlocfilehash: 112f77738b33aae94babe0cf8e9e61ff2ea3d004
ms.contentlocale: tr-tr
ms.lasthandoff: 05/22/2018

---

# <a name="specify-the-cross-rate"></a><span data-ttu-id="ad400-103">Çapraz kuru belirtme</span><span class="sxs-lookup"><span data-stu-id="ad400-103">Specify the cross rate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ad400-104">Bu konu, çapraz kurun amacını ve faturaya karşılık bir ödemeyi kapattığınız zaman çapraz kurun nasıl belirtileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="ad400-104">This topic explains the purpose of a cross rate, and how to specify the cross rate when you settle a payment with an invoice.</span></span> <span data-ttu-id="ad400-105">Aşağıdaki ölçütlerin tümü geçerliyse bir çapraz kur kullanın:</span><span class="sxs-lookup"><span data-stu-id="ad400-105">Use a cross rate when all of the following criteria apply:</span></span> 
-   <span data-ttu-id="ad400-106">Faturaya karşılık bir ödemeyi kapatıyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="ad400-106">You are settling a payment with an invoice.</span></span> 
-   <span data-ttu-id="ad400-107">Ödeme satırı ve fatura satırı farklı para birimleri kullanıyor.</span><span class="sxs-lookup"><span data-stu-id="ad400-107">The payment line and the invoice line use different currencies.</span></span> 
-   <span data-ttu-id="ad400-108">Para birimlerinin her ikisi de muhasebe para birimi değil.</span><span class="sxs-lookup"><span data-stu-id="ad400-108">Neither currency is the accounting currency.</span></span> 

<span data-ttu-id="ad400-109">Çapraz kur, ödeme hareketi para birimini ödeme muhasebe para birimine dönüştürmeyi hesaplamak için kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="ad400-109">The cross rate is not used to calculate the payment transaction currency translation to the payment accounting currency.</span></span> <span data-ttu-id="ad400-110">Bunun yerine, ödeme hareketinin para birimi tutarı ve ödeme muhasebe para birimi tutarı değerini hesaplamak için döviz kurları tablolarından döviz kurları alınır.</span><span class="sxs-lookup"><span data-stu-id="ad400-110">Instead, the exchange rates from the exchange rate tables are retrieved to calculate the value of the payment transaction currency amount and the payment accounting currency amount.</span></span> 

<span data-ttu-id="ad400-111">Örneğin, muhasebe para birimi USD, fatura para birimi CAD ve ödeme para birimi EUR olsun.</span><span class="sxs-lookup"><span data-stu-id="ad400-111">For example, the accounting currency is USD, the invoice currency is CAD, and the payment currency is EUR.</span></span> <span data-ttu-id="ad400-112">Çapraz kur, CAD ve EUR arasında doğrudan (USD üzerinden dönüştürmeye gerek kalmadan) dönüştürmek için bir döviz kuru girmenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="ad400-112">The cross rate lets you enter an exchange rate to translate directly between CAD and EUR, and not have to translate through USD.</span></span> <span data-ttu-id="ad400-113">Bir fatura ve bir birincil ödeme seçerken fatura satırı için bir çapraz kur girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ad400-113">When you select an invoice and a primary payment, you can enter a cross rate for the invoice line.</span></span> <span data-ttu-id="ad400-114">Çapraz kur, kapatma tarihi itibariyle bu hareketlerin para birimleri arasındaki döviz kurudur.</span><span class="sxs-lookup"><span data-stu-id="ad400-114">The cross rate is the exchange rate between the currencies for those transactions, as of the settlement date.</span></span>

1.  <span data-ttu-id="ad400-115">Aşağıdaki sayfalardan birine gidin:</span><span class="sxs-lookup"><span data-stu-id="ad400-115">Go to one of the following pages:</span></span>
- <span data-ttu-id="ad400-116">**Alacak hesapları > Genel > Müşteriler > Tüm müşteriler**</span><span class="sxs-lookup"><span data-stu-id="ad400-116">**Accounts receivable > Common > Customers > All customers**</span></span> 
- <span data-ttu-id="ad400-117">**Borç hesapları > Genel > Satıcılar > Tüm satıcılar**</span><span class="sxs-lookup"><span data-stu-id="ad400-117">**Accounts payable > Common > Vendors > All vendors**</span></span> 
- <span data-ttu-id="ad400-118">**Tedarik ve kaynak atama > Genel > Satıcılar > Tüm satıcılar**</span><span class="sxs-lookup"><span data-stu-id="ad400-118">**Procurement and sourcing > Common > Vendors > All vendors**</span></span>
2.  <span data-ttu-id="ad400-119">Açık hareketlerini kapattığınız müşteri veya satıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="ad400-119">Select the customer or vendor whose open transactions you are settling.</span></span> 
3.  <span data-ttu-id="ad400-120">Müşteri için, **Tüm müşteriler** liste sayfasında **Tahsil et > Açık hareketleri kapat**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="ad400-120">For a customer, on the **All customers** list page, go to **Collect > Settle open transactions**.</span></span> <span data-ttu-id="ad400-121">Satıcı için, **Tüm satıcılar** liste sayfasında **Fatura > Açık hareketleri kapat**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="ad400-121">For a vendor, on the **All vendors** list page, go to **Invoice > Settle open transactions**.</span></span> 
4.  <span data-ttu-id="ad400-122">Birincil ödeme olan hareketi seçin ve **Ödemeyi işaretle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ad400-122">Select the transaction that is the primary payment, and then click **Mark payment**.</span></span> <span data-ttu-id="ad400-123">**İşaret** sütunundaki onay kutusu işaretlenir ve **Birincil ödeme** sütununda bir bilgi simgesi görünür.</span><span class="sxs-lookup"><span data-stu-id="ad400-123">The check box in the **Mark** column is selected, and an information icon is shown in the **Primary payment** column.</span></span> 
5.  <span data-ttu-id="ad400-124">**Çapraz kur** alanına, fatura para birimi ve ödeme para birimi arasında kapatma tarihi itibariyle geçerli olan döviz kurunu girin.</span><span class="sxs-lookup"><span data-stu-id="ad400-124">In the **Cross rate** field, enter the exchange rate between the invoice currency and the payment currency, as of the settlement date.</span></span> 
