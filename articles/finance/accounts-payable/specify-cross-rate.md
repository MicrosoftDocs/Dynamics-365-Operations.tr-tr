---
title: Çapraz kuru belirtme
description: Bu konuda, Microsoft Dynamics 365 Finance'teki çapraz kurlar hakkında bilgi verilmektedir.
author: abruer
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 317cad877cec4d9f02f53762af65f0b226d0aad6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979400"
---
# <a name="specify-the-cross-rate"></a><span data-ttu-id="6adda-103">Çapraz kuru belirtme</span><span class="sxs-lookup"><span data-stu-id="6adda-103">Specify the cross rate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6adda-104">Bu konu, çapraz kurun amacını ve faturaya karşılık bir ödemeyi kapattığınız zaman çapraz kurun nasıl belirtileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="6adda-104">This topic explains the purpose of a cross rate, and how to specify the cross rate when you settle a payment with an invoice.</span></span> <span data-ttu-id="6adda-105">Aşağıdaki ölçütlerin tümü geçerliyse bir çapraz kur kullanın:</span><span class="sxs-lookup"><span data-stu-id="6adda-105">Use a cross rate when all of the following criteria apply:</span></span> 
-   <span data-ttu-id="6adda-106">Faturaya karşılık bir ödemeyi kapatıyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="6adda-106">You are settling a payment with an invoice.</span></span> 
-   <span data-ttu-id="6adda-107">Ödeme satırı ve fatura satırı farklı para birimleri kullanıyor.</span><span class="sxs-lookup"><span data-stu-id="6adda-107">The payment line and the invoice line use different currencies.</span></span> 
-   <span data-ttu-id="6adda-108">Para birimlerinin her ikisi de muhasebe para birimi değil.</span><span class="sxs-lookup"><span data-stu-id="6adda-108">Neither currency is the accounting currency.</span></span> 

<span data-ttu-id="6adda-109">Çapraz kur, ödeme hareketi para birimini ödeme muhasebe para birimine dönüştürmeyi hesaplamak için kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="6adda-109">The cross rate is not used to calculate the payment transaction currency translation to the payment accounting currency.</span></span> <span data-ttu-id="6adda-110">Bunun yerine, ödeme hareketinin para birimi tutarı ve ödeme muhasebe para birimi tutarı değerini hesaplamak için döviz kurları tablolarından döviz kurları alınır.</span><span class="sxs-lookup"><span data-stu-id="6adda-110">Instead, the exchange rates from the exchange rate tables are retrieved to calculate the value of the payment transaction currency amount and the payment accounting currency amount.</span></span> 

<span data-ttu-id="6adda-111">Örneğin, muhasebe para birimi USD, fatura para birimi CAD ve ödeme para birimi EUR olsun.</span><span class="sxs-lookup"><span data-stu-id="6adda-111">For example, the accounting currency is USD, the invoice currency is CAD, and the payment currency is EUR.</span></span> <span data-ttu-id="6adda-112">Çapraz kur, CAD ve EUR arasında doğrudan (USD üzerinden dönüştürmeye gerek kalmadan) dönüştürmek için bir döviz kuru girmenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="6adda-112">The cross rate lets you enter an exchange rate to translate directly between CAD and EUR, and not have to translate through USD.</span></span> <span data-ttu-id="6adda-113">Bir fatura ve bir birincil ödeme seçerken fatura satırı için bir çapraz kur girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6adda-113">When you select an invoice and a primary payment, you can enter a cross rate for the invoice line.</span></span> <span data-ttu-id="6adda-114">Çapraz kur, kapatma tarihi itibariyle bu hareketlerin para birimleri arasındaki döviz kurudur.</span><span class="sxs-lookup"><span data-stu-id="6adda-114">The cross rate is the exchange rate between the currencies for those transactions, as of the settlement date.</span></span>

1.  <span data-ttu-id="6adda-115">Aşağıdaki sayfalardan birine gidin:</span><span class="sxs-lookup"><span data-stu-id="6adda-115">Go to one of the following pages:</span></span>
- <span data-ttu-id="6adda-116">**Alacak hesapları > Genel > Müşteriler > Tüm müşteriler**</span><span class="sxs-lookup"><span data-stu-id="6adda-116">**Accounts receivable > Common > Customers > All customers**</span></span> 
- <span data-ttu-id="6adda-117">**Borç hesapları > Genel > Satıcılar > Tüm satıcılar**</span><span class="sxs-lookup"><span data-stu-id="6adda-117">**Accounts payable > Common > Vendors > All vendors**</span></span> 
- <span data-ttu-id="6adda-118">**Tedarik ve kaynak atama > Genel > Satıcılar > Tüm satıcılar**</span><span class="sxs-lookup"><span data-stu-id="6adda-118">**Procurement and sourcing > Common > Vendors > All vendors**</span></span>
2.  <span data-ttu-id="6adda-119">Açık hareketlerini kapattığınız müşteri veya satıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="6adda-119">Select the customer or vendor whose open transactions you are settling.</span></span> 
3.  <span data-ttu-id="6adda-120">Müşteri için, **Tüm müşteriler** liste sayfasında **Tahsil et > Açık hareketleri kapat**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="6adda-120">For a customer, on the **All customers** list page, go to **Collect > Settle open transactions**.</span></span> <span data-ttu-id="6adda-121">Satıcı için, **Tüm satıcılar** liste sayfasında **Fatura > Açık hareketleri kapat**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="6adda-121">For a vendor, on the **All vendors** list page, go to **Invoice > Settle open transactions**.</span></span> 
4.  <span data-ttu-id="6adda-122">Birincil ödeme olan hareketi seçin ve **Ödemeyi işaretle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6adda-122">Select the transaction that is the primary payment, and then click **Mark payment**.</span></span> <span data-ttu-id="6adda-123">**İşaret** sütunundaki onay kutusu işaretlenir ve **Birincil ödeme** sütununda bir bilgi simgesi görünür.</span><span class="sxs-lookup"><span data-stu-id="6adda-123">The check box in the **Mark** column is selected, and an information icon is shown in the **Primary payment** column.</span></span> 
5.  <span data-ttu-id="6adda-124">**Çapraz kur** alanına, fatura para birimi ve ödeme para birimi arasında kapatma tarihi itibariyle geçerli olan döviz kurunu girin.</span><span class="sxs-lookup"><span data-stu-id="6adda-124">In the **Cross rate** field, enter the exchange rate between the invoice currency and the payment currency, as of the settlement date.</span></span> 
