---
title: Proje faturalama
description: Bu makalede, Zaman ve malzeme projeleri ve Sabit fiyatlı projeler için proje faturalamaya genel bir bakış verilmektedir. Fatura teklifleri (ön faturalar), fatura kontrolü, hesaba mahsup faturalama, satıcı faturalama ve hakkındaki bilgileri içerir ve alacak dekontları hakkında bilgiler içermektedir.
author: TaylorVH
ms.date: 07/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjInvoiceCashFlow, ProjInvoiceControl, ProjInvoiceListPage, ProjInvoiceProposalDetail, ProjInvoiceProposalListPage
audience: Application User, IT Pro
ms.reviewer: zezhangzhao
ms.custom: 23111
ms.assetid: 1812d6f2-8b34-4258-8f5f-dcf12281547f
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-07-06
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 4af44127d80c943ed9cebeac21d7e9c8372910f3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861690"
---
# <a name="project-invoicing"></a>Proje faturalama

[!include [banner](../includes/banner.md)]

Bu makalede, Zaman ve malzeme projeleri ve Sabit fiyatlı projeler için proje faturalamaya genel bir bakış verilmektedir. Fatura teklifleri (ön faturalar), fatura kontrolü, hesaba mahsup faturalama, satıcı faturalama ve hakkındaki bilgileri içerir ve alacak dekontları hakkında bilgiler içermektedir.

Proje tipi, hangi faturalama prosedürünün uygulanacağını belirler. Sadece iki harici proje türü, Zaman ve malzeme ve Sabit fiyatlı, faturalandırılabilir. Zaman ve malzeme projeleri ile sabit fiyatlı projeler her zaman bir proje sözleşmesine iliştirilir.

-   **Sabit fiyatlı projeler** – Müşteri faturası tutarı, faturalama planlarına dayanır. Faturalama, aynı zamanda faturalama planı olarak da adlandırılan bir açık hesap kurulumu ile yapılır. Sabit fiyatlı projeler proje başına veya proje sözleşmesi başına faturalanabilir.
-   **Zaman ve malzeme projeleri**– Müşteri faturası tutarı, projelere girilen hareket satırlarına dayanır. Hareketler proje veya proje sözleşmesi başına faturalanabilir.

Zaman ve malzeme projeleri ile sabit fiyatlı projeleri fatura projelerine iliştirmenin üç yolu vardır:

-   **Açık hesap faturalama** – Zaman ve malzeme projeleri ile sabit fiyatlı projeler açık hesap şeklinde faturalanabilir. Her proje türü için iki tür açık hesap ayarı gerekir.
-   **Periyodik bölümde faturalama** - Hareketler, periyodik işlevler yoluyla projeler arasında faturalanabilir. Ayrıca, periyodik işlevleri, faturalanması zorunlu hareketlere yönelik bir genel bakış da sağlamaktadır.
-   **Faturada alacak dekontu kullanarak** - Alacak dekontu hem zaman ve malzeme projeleri, hem de sabit fiyatlı projeler için oluşturulabilir.

## <a name="invoice-proposals"></a>Fatura teklifleri
Bir proje için bir müşteri faturası oluşturmadan önce, ön fatura ya da fatura teklifi oluşturabilirsiniz. Bir fatura teklifinde, bir proje faturasına dahil edilecek proje hareketlerini seçebilirsiniz. Daha sonra, proje faturasını deftere nakletmeden veya müşteri veya diğer finans kaynağına göndermeden önce fatura ayrıntılarını gözden geçirebilirsiniz.

### <a name="creating-invoice-proposals"></a>Fatura teklifleri oluşturma

Fatura tekliflerini belirtilen proje için bir kullanılabilir hareket listesinden el ile seçerek oluşturabilirsiniz. Ayrıca, ne zaman otomatik olarak bir fatura teklifi oluşturulacağını belirten faturalama kuralları da ayarlayabilirsiniz. Örneğin, Faturalama projesi üzerinde çalışmanın yüzde 25, yüzde 50, yüzde 75'i ve yüzde 100'ü tamamlanmış olduğunda bir fatura teklifi oluşturmak için kural oluşturabilirsiniz. 

Aşağıdaki hareketler için fatura teklifleri oluşturabilirsiniz:

-   Saatler, giderler ve diğer proje hareketleri
-   Önceki proje faturalarında müşteriler tarafından kesilen tutarlar
-   Alacak dekontları
-   Proje başlamadan önce bir müşteri tarafından size yapılan ödeme tutarları

> [!NOTE]
> **Proje fatura teklifi oluşturma sırasında kaynağa göre sıralamayı etkinleştir** özelliği proje muhasebecinin, yeni bir proje faturası teklifi oluştururken kaynak tarafından faturalamada kullanılabilen proje hareketlerini sıralamasına olanak tanır. Kullanılabilir proje hareketlerinin görüntülendiği kılavuzda **Kaynak kimliği** ve **Kaynak** için ayrı alanlar olur. Bu alanlar kaynak adına filtre ve sıralama uygulamanızı sağlar. Bu özellik, varsayılan olarak kapalıdır. **Özellik yönetimi** sayfası (**Çalışma alanları > Özellik yönetimi**) kullanılarak etkinleştirilebilir. Bu özelliği etkinleştirme konusunda yardım için sistem yöneticinize başvurun.

Bir fatura teklifinde ücret hareketleri oluşturabilirsiniz. Ayrıca saat, gider, madde ve ücret hareketlerinin satış fiyatı üzerinde değişiklik yapabilirsiniz. Bir fatura teklifini deftere naklettiğinizde, güncel fiyatlar ve hareketler proje raporları ve hareket geçmişine eklenir. 

Bir proje için birden fazla müşteri faturası oluşturmak için, her fatura için bir fatura teklifi oluşturmanız gerekir. Örneğin, hareket türüne göre fatura oluşturabilirsiniz. Saatleri bir müşteri faturasında ve kalemleri bir diğer faturada belirtmek için saat hareketleri ve ücret hareketleri için ayrı fatura teklifleri oluşturmanız gerekir. 

Bir projenin birden fazla finansman kaynağı varsa, her finansman kaynağı için ayrı bir fatura teklifi oluşturabilirsiniz. **Finansman kuralları** sayfasında, hareketin her bir finansman kaynağına tahsis edilecek yüzdesini tanımlayabilir ve yuvarlama farklarınının nakledileceği kaynağı da belirtebilirsiniz.

### <a name="creating-customer-invoices-from-invoice-proposals"></a>Fatura tekliflerinden müşteri faturaları oluşturma

Bir fatura teklifini oluşturduktan ve naklettikten sonra, fatura teklifine dahil olan hareketleri içeren bir müşteri faturası otomatik olarak oluşturulur. 

Bir fatura teklifini deftere nakletmeden önce bunun üzerine hareketleri ekleyebilir veya silebilirsiniz. Örneğin, bir proje için deftere nakledilen fakat müşteriye borçlandırılabilir olmayan masraf hareketlerini kaldırabilirsiniz. 

Kuruluşunuz, nakledilmeden önce fatura tekliflerinin incelenmesi gerektiriyorsa, fatura teklifini deftere nakletmeden önce "Proje Fatura tekliflerini inceleme" iş akışının onayından geçmesi gerekebilir.

### <a name="view-grant-information-on-project-invoice-list-pages"></a>Proje fatura listesi sayfalarında izin bilgilerini görüntüleme

Kamu sektörü kullanıcıları **Proje faturası teklifleri** ve **Proje faturaları** listesi sayfalarına **İzin kodu** ve **İzin adı** ekleyebilir. Bu sütunlar, **Proje fatura listesi sayfalarına izin bilgisi ekle** özelliği kullanılarak etkinleştirilir. Bu özellik varsayılan olarak kapalıdır ve **Çalışma alanları > Özellik yönetimi**'nde etkinleştirilebilir. Bu özelliği etkinleştirme konusunda yardım için sistem yöneticinize başvurun.

## <a name="on-account-invoicing"></a>Açık hesap faturalama
Bir proje için açık hesap faturasına girdiğiniz tutar zamanlamaya, tamamlanma yüzdesine ve ilgili proje sözleşmesinde belirtilmiş olan diğer faturalama koşullarına dayalıdır Tutar, projeye nakledilen saatler, maddeler, giderler veya ücretlere dayanarak hesaplanmamıştır. 

Bu açık hesap hareketini proje faturasına ekleyebilmeden önce, zaman ve malzeme projesi veya sabit fiyatlı bir proje için bir açık hesap hareketi oluşturmalısınız. Açık hesap hareketi üzerinde, müşteriye faturalanacak tutarı girin. Tutar için bir proje faturası oluşturmak için, ön fatura (fatura teklifi) oluşturun. Fatura teklifinde, açık hesap hareketini seçin. Bunun için bir proje faturası oluşturmadan önce açık hesap bilgisini fatura teklifinde gözden geçirebilirsiniz. 

### <a name="fixed-price-projects"></a>Sabit fiyatlı projeler
Sabit fiyatlı projeler için açık hesap hareketleri proje sözleşmesinde üzerinde anlaşılmış olan kilometre taşı, teslimat birimi veya hak ediş bazında faturalamayı temel alır. Proje müşteriden alınması gereken her bir ödeme için bir satır oluşturulur. Kesintilere gerek yoktur.

### <a name="time-and-material-projects"></a>Zaman ve malzeme projeleri.

Zaman ve malzeme projeleri için müşteri veya diğer fon kaynağı için peşinat tutarını bir açık hesap fatura teklifini kullanarak fatura edebilirsiniz. Açık hesap hareketlerini bir satır olarak gir. İsteğe bağlı olarak, müşterinin yapmış olduğu ödemeleri kesinti olarak mahsup etmek için ek satırlar girebilirsiniz. Kesinti satırları oluşturmak için tutarın önüne eksi işareti girin.

## <a name="invoice-control"></a>Fatura kontrol
Fatura kontrolünü faturalandırılmış ve faturalandırılmamış hareketleri izlemek ve bu hareketleri projelerinizin, tekliften tamamlamaya, uçtan uca görünümü için tekliflere karşı çözümleyebilirsiniz. Hangi hareketlerin belirli bir projeye ücretlendirildiklerini ve hangi satırların faturalandırıldığını görebilirsiniz. Ayrıca, tek tek hareketleri görebilir ve böylece deftere nakledildikten sonra bu hareketleri düzeltebilirsiniz.

## <a name="invoicing-fixed-price-projects"></a>Sabit fiyatlı projeleri faturalandırma
Sabit fiyatlı bir projeyi faturalandırmak için fatura zamanlamasını tanımlamak ve faturalandırma yordamını tamamlamalısınız.

### <a name="billing-schedule"></a>Faturalama çizelgesi

Sabit fiyatlı projeleri faturalama zamanlamasında faturalayabilirsiniz. Faturalama zamanlaması, proje için bir ya da daha fazla kilometre taşı ile tanımlanır. Her kilometre taşı için belirli bir tarih, satış para birimi, satış fiyatı ve etkinlik tanımlayabilirsiniz. 

Örneğin, aşağıdaki faturalama zamanlamasını takip edebilirsiniz:

-   Proje sözleşmesi imzalandığında yüzde 20
-   İlk teslimatta yüzde 30
-   İkinci teslimatta yüzde 15
-   Son teslimatta yüzde 35

### <a name="invoicing-procedure"></a>Faturalandırma yordamı

Kilometre taşı ödemeleri faturalandırmaya hazır olduğunda, yordamı açık hesap tutarları faturalandırmak için yordamı kullanın.

## <a name="vendor-invoicing"></a>Satıcı faturalandırması
Bir maddeyi bir satıcıdan sipariş edip bir projeye atadığınızda, bu madde için satınalma siparişi satırında seçtiğiniz satır özelliği, satın alınan maddenin müşteriye fatura edilip edilmeyeceğini belirler. Varsayılan satır özelliklerini ayarlarsanız bunlar satın alma siparişi satırındaki kalem için görüntülenir (**Satır ayrıntıları > Proje > Satır özelliği tutarları**). Satır özelliğini değiştirmenin iki yolu vardır:

-   Proje müşterisine kalem için fatura kesin. Bunun için kalem satır özelliğini satın alma siparişine ücrete tabi değerine ayarlayın ve sonra doğru proje faturalama yöntemini kullanarak müşteriye fatura edin.
-   Proje müşterisine kalem için fatura kesmeyin. Bunu yapmak için kalemin satın alma siparişi satırında **Borçlandırılabilir** satır özelliğini seçmeyin. Sonra satınalma siparişini faturalayabilirsiniz ve başka bir eyleme gerek yoktur.

> [!NOTE] 
> Serbest bırakma tutma satırları varsayılan olarak masraflandırılamaz. Bu, serbest bırakılan tutma için fatura teklifi oluşturma özelliğinin etkinleştirilmediği anlamına gelir.

## <a name="credit-notes"></a>Alacak dekontları
Bir müşteri faturası üzerindeki tutarın negatif değeri olması durumunda, fatura bir alacak dekontu olarak sınıflandırılır. Belge yazdırıldığında, başlığı "Kredi notu" olur. 

Önceden faturalanmış bir tutarı alacaklandırmak üzere bir alacak dekontu oluşturduğunuzda, öncelikle alacaklandırmak üzere faturalandırılan tutarı seçmeniz gerekir. Ardından, bir alacak dekontunu bir sıradan müşteri faturasını oluşturmak için kullanılan aynı prosedürü izleyerek oluşturursunuz. Daha önce bir müşteri faturasında nakledilmiş hareketleri seçip, ardından bir alacak dekontu teklifini oluşturur ve deftere nakledersiniz. 

Aynı belge alacaklandırma için seçilenleri, alacak hareketlerini ve deftere nakledilmiş hareketleri içerebilir. Bu belgenin sınıflandırması, toplam tutarın pozitif veya negatif olup olmamasına bağlı olarak, bir fatura veya bir alacak dekontu olacaktır. 

Faturalandırmış bir tutarı alacaklandırmak için, önce alacaklandırmak için faturalandırılmış tutarı seçin ve sonra alacak dekontunu oluşturun. Bir alacak dekontunu bir müşteri faturasını oluşturmak için kullanacağınız aynı prosedürü izleyerek oluşturursunuz. 

Bir alacak dekontu olarak sınıflandırılacak bir fatura haline gelecek, negatif tutara sahip bir fatura oluşturabilirsiniz. Bir alacak dekontunu oluşturmak ve yazdırmak için daha önce bir müşteri faturası için deftere nakledilen hareketleri seçmeli ve ardından hareketlerinde değişiklik yapmalısınız. Tüzel kişiliğin birincil adresi Almanya'da olmadığı sürece, faturanın başlığı "Düzeltme faturası" olacaktır.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
