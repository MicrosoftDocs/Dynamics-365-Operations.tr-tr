---
title: Kapatma yapılandırma
description: Hareketlerin neden ve ne zaman kapatıldığı karmaşık konular olabilir. O yüzden, iş gereksinimlerinizi karşılayacak parametreleri doğru bir şekilde anlayıp tanımlamanız çok önemlidir. Bu konuda, hem Borç hesapları hem Alacak hesapları için kapanışta kullanılan parametreler açıklanmaktadır.
author: kweekley
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, CustParameters, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: 14601
ms.assetid: 6b61e08c-aa8b-40c0-b904-9bca4e8096e7
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 323a1e6d426208a880a72dd89f7be04bacbf13a8e6c5d8ab7599217cfc18f2c0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720586"
---
# <a name="configure-settlement"></a>Kapatma yapılandırma

[!include [banner](../includes/banner.md)]

Hareketlerin neden ve ne zaman kapatıldığı karmaşık konular olabilir. O yüzden, iş gereksinimlerinizi karşılayacak parametreleri doğru bir şekilde anlayıp tanımlamanız çok önemlidir. Bu konuda, hem Borç hesapları hem Alacak hesapları için kapanışta kullanılan parametreler açıklanmaktadır. 

Aşağıdaki parametreler, Microsoft Dynamics 365 Finance'da kapatmaların nasıl işleneceğini etkiler. Kapatma işlemi bir faturanın bir ödemeye veya bir alacak dekontuna karşılık kapatılmasını içerir. Bu parametreler **Alacak hesapları parametreleri** ve **Borç hesapları parametreleri** sayfalarının **Kapatma** alanında bulunur.

- **Otomatik kapatma** – Nakledildiğinde bir hareketin diğer açık hareketlere karşılık otomatik olarak kapatılması gerekiyorsa bu seçeneği **Evet** konumuna ayarlayın. Bu seçenek **Hayır** olarak ayarlanırsa kullanıcılar, ödemeleri girdiğinde veya daha sonra **Hareketleri kapat** sayfasını kullanarak hareketleri el ile kapatabilirler.
- **Nakit iskontosu yönetimi** – Bir [nakit iskontosunun fatura fazla ödendiğinde nasıl yönetileceğini belirtir](cash-discount-handling-overpayments.md). Fazla ödeme için, nakit iskontosu azaltılabilir, fark olarak kabul edilebilir veya satıcı veya müşteri hesabında kalabilir.
  -   **Belirsiz** – Nakit iskontosu tutarı, fazla ödeme tutarıyla giderilir. Bu davranış, fazla ödeme tutarının **Maksimum fazla ödeme veya eksik ödeme** alanına girilen miktardan fazla veya düşük olup olmamasından bağımsız olarak her zaman uygulanır.
  -   **Özel** – Fazla ödeme tutarı bir nakit iskontosu farkı defter hesabına nakledilir veya müşteri veya satıcı hesabında bir bakiye olarak kalır. Bu özel davranış, fazla ödeme tutarının 0.00 ile **Maksimum fazla ödeme veya eksik ödeme** alanında belirlenen tutar arasında olup olmadığına veya fazla ödeme tutarının **Maksimum fazla ödeme veya eksik ödeme** tutarından yüksek olup olmadığına göre değişir.
- **Maksimum kuruş farkı** – Kapatılan hareketler için izin verilen maksimum kuruş farkını girin. Fark, bu alanda belirtilen kuruş farkına eşit veya daha düşükse fark, **Otomatik hareket hesapları** sayasında belirtilen kuruş farkı genel muhasebe hesabına nakledilecektir.
- **Maksimum fazla ödeme veya eksik ödemedeki** – Fazla ödeme veya eksik ödeme olarak kabul edilecek tutarı girin. Fazla veya eksik ödemelerdeki vergiyi hesaplamak için, **Genel muhasebe parametreleri** sayfasında **Satış vergisi** öğesini tıklayın ve ardından **Fazla veya eksik ödemedeki satış vergisi** seçeneğini işaretleyin.
  -   Fazla ödeme veya eksik ödeme, **Maksimum kuruş farkı** alanında tanımlanan farktan daha az kuruş farkı oluşturursa, kuruş farkı tutarı kuruş farkı hesabına nakledilir.
  -   Fazla ödeme veya eksik ödeme, **Maksimum kuruş farkı** alanında tanımlanan farktan daha fazla bir fark üretiyorsa fark tutarı, **Otomatik hareketler için hesaplar** sayfasındaki **Müşteri nakit iskontosu** veya **Satıcı nakit iskontosu** nakil türü için seçilen fark hesabına nakledilir.
- **Kısmi ödemeler için nakit iskontolarını hesapla** – Nakit iskontolarının kısmi ödemeler için otomatik olarak hesaplanmasını sağlamak için bu seçeneği **Evet** konumuna ayarlayın.
  -   Bu seçeneğin etkisi, **Hareketleri kapat** sayfasındaki **Nakit iskontosu kullan** alanının değerine bağlıdır. Bu seçenek **Evet** konumuna ayarlanırsa, **Nakit iskontosu kullan** alanı **Normal** konumuna ayarlandığında iskonto alınır. **Nakit iskontosu kullan** alanı **Her zaman** konumuna ayarlanırsa bu alanın ayarından bağımsız olarak her zaman nakit iskontosu alınır. **Nakit iskontosu kullan** alanı **Hiçbir zaman** konumuna ayarlanırsa bu alanın ayarından bağımsız olarak hiçbir zaman nakit iskontosu alınmaz.
  -   Bu seçenek **Evet** konumuna ayarlanırsa ve kullanıcı, **Hareketleri kapat** sayfasındaki **Kapatılacak tutar** alanındaki değeri değiştirirse, iskonto otomatik olarak hesaplanır ve **Alınacak nakit iskonto tutarı** alanında varsayılan giriş olarak görüntülenir.
  -   Bu seçenek **Hayır** olarak ayarlanırsa ve bir kullanıcı **Hareketleri kapat** sayfasındaki **Kapatılacak tutar** alanındaki bir değeri değiştirirse, **Alınacak nakit iskontosu tutarı** alanındaki varsayılan giriş **0** (sıfır) olur.
- **Alacak dekontları için nakit iskontoları hesapla** – Alacak dekontları için bir nakit iskontosunu otomatik olarak hesaplamak için bu seçeneği **Evet** konumuna ayarlayın. Alacak hesaplarında bir alacak dekontu hareketi **Serbest metin faturası** sayfasındaki **Fatura** alanında bir değere veya **Satış emri** sayfasında bir iadeye sahip olan bir negatif harekettir.
  - Bu seçeneğin etkisi, <strong>Hareketleri kapat</strong> sayfasındaki <strong>Nakit iskontosu kullan</strong> alanının değerine bağlıdır. Bu seçenek <strong>Evet</strong> konumuna ayarlanırsa, *<strong><em>Nakit iskontosu kullan</em></strong>* alanı <strong>Normal</strong> konumuna ayarlandığında iskonto alınır. *<strong><em>Nakit iskontosu kullan</em></strong>* alanı <strong>Her zaman</strong> konumuna ayarlanırsa bu alanın ayarından bağımsız olarak her zaman nakit iskontosu alınır. *<strong><em>Nakit iskontosu kullan</em></strong>* alanı <strong>Hiçbir zaman</strong> konumuna ayarlanırsa bu alanın ayarından bağımsız olarak hiçbir zaman nakit iskontosu alınmaz.
  - Bu seçenek **Evet** konumuna ayarlanır ve **Hareketleri kapat** sayfasında bir alacak dekontu işaretlenirse, iskonto otomatik olarak hesaplanır ve **Alınacak nakit iskonto tutarı** alanında varsayılan giriş olarak görüntülenir.
  - Bu seçenek **Hayır** konumuna ayarlanırsa ve **Hareketleri kapat** sayfasında bir alacak dekontu işaretlenirse, **Alınacak nakit iskonto tutarı** alanındaki varsayılan giriş **0**'dır (sıfır).

- **İskonto mahsup hesapları (yalnızca AP)** – Nakit iskontoları muhasebe girişi için kullanılacak varsayılan nakit iskontosu genel muhasebe hesabını tanımlayın.
  -   **Satıcı iskontoları için Ana hesabı kullan** – Nakit iskontosu **Nakit iskontosu kurulumu** sayfasında tanımlanan ana hesaba aktarılır.
  -   **Fatura satırlarındaki hesaplar** – Nakit iskontosu, orijinal fatura üzerindeki genel muhasebe hesaplarına nakledilir.
- **Serbest metin faturalarındaki ve vade farkı dekontlarındaki satırları işaretle (yalnızca AR)** – Bu seçeneği **Evet** konumuna getirerek **Müşteri ödemelerini gir**, **Ödeme günlüğü fişi** ve **Hareketleri kapat** sayfalarındaki **Fatura satırlarını işaretle** düğmesini etkinleştirin. Bu düğme kullanıcının kapatma için tek tek satırları işaretlemesini sağlar.
- **Kapatmaya öncelik belirle (yalnızca AR)** – Bu seçeneği **Evet** konumuna getirerek **Müşteri ödemelerini gir** ve **Hareketleri kapat** sayfalarındaki **Önceliğe göre işaretle** düğmesini etkinleştirin. Bu düğme, kullanıcıların önceden belirlenmiş kapama siparişlerini hareketlere atamalarını sağlar.  Bir harekete kapatma siparişi uygulandıktan sonra, sipariş ve ödeme tahsisatı deftere nakilden önce değiştirilebilir.
- **Otomatik kapatmalar için öncelik kullan** – Hareketler otomatik kapatıldıklarında belirlenmiş önceliği kullanmak için bu seçeneği **Evet** olarak ayarlayın. Bu alan yalnızca **Kapanışa öncelik ver** ve **Otomatik kapanış** seçenekleri **Evet** olarak ayarlanmışsa kullanılabilir.

## <a name="fixed-dimensions-on-accounts-receivableaccounts-payable-main-accounts"></a>Alacak hesapları/borç hesapları ana hesaplarında sabit boyutlar

Sabit boyutlar, hesapları alacak hesapları/borç hesapları ana hesabı ek muhasebe girişlerinde kullanılır ve kapatma işlemiyle iki ek satıcı hareketi nakledilir. Kapatma, hesapları alacak hesapları/borç hesapları genel muhasebe hesabının faturadaki ve ödemedeki değerlerini karşılaştırır.  Ödeme ve kapatma birlikte tamamlandığında (tipik senaryo), ödemenin muhasebe girişi, kapatma işlemi de tamamlanana kadar Genel muhasebeye nakledilmez. İşlem olayları sırası nedeniyle, kapatma, gerçek alacak hesapları/borç hesapları genel muhasebe hesabını, ödemenin muhasebe girişinden belirleyemez. Kapatma, ödeme için genel muhasebe hesabının ne olacağını yeniden oluşturur. Alacak hesapları/borç hesapları ana hesabı için sabit bir boyut kullanıldığında bu bir sorun oluşturur.

Genel muhasebe hesabını yeniden oluşturmak için, alacak hesapları/borç hesapları ana hesabı deftere nakil profilinden ve mali boyutlar, ödeme günlüğünde tanımlandığı gibi, ödeme için satıcı hareketi kaydından alınır. Sabit boyutlar ödeme günlüklerinde varsayılan yapılmaz; bunun yerine, deftere nakil işleminin son adımı olarak ana hesaba uygulanır. Sonuç olarak, sabit boyut değeri, satıcı gibi bir başka kaynaktan varsayılan olarak alınmıyorsa, büyük olasılıkla satıcı hareketinde yer almaz. Yeniden oluşturulan hesap, sabit boyutu içermeyecektir. Kapatma işlemi bir ayarlama girişi oluşturulması gerektiğini belirler çünkü sabit boyut değeriyle nakledilen fatura ve yeniden oluşturulan ödeme hesabı eşleşmemiştir.  Kapatma işlemi, ayarlama girişiyle deftere nakil işlemine geçtiği için, deftere nakilde son adım, uygulanacak sabit boyuta ilişkindir. Ayarlama girişine sabit boyut eklenerek, aynı genel muhasebe hesabına bir borç ve alacakla nakledilir. Kapatma, muhasebe girişini geri alamaz.

Ek muhasebe girişlerini (aynı genel muhasebe hesabına borç ve alacak girişi) önlemek için, iş gereksinimlerinize bağlı olarak aşağıdaki geçici çözümler değerlendirilmelidir. 

-   Kuruluşlar gerekli olmayan bir mali boyutu sıfırla doldurmak için sık sık sabit boyutları kullanılır. Bu genellikle alacak hesapları/borç hesapları gibi bilanço hesapları için geçerlidir. Hesap yapıları tipik olarak sıfırla doldurulmuş mali boyutları izlememek için kullanılabilir.  Bilanço hesapları için mali boyutu kaldırarak, sabit boyutları kullanma gereksinimini ortadan kaldırabilirsiniz.
-   Kuruluşunuz alacak hesapları/borç hesapları ana hesabında sabit boyutları gerektiriyorsa, sabit boyutu ödemede varsayılan yapmanın bir yolunu bularak, sabit boyut değerinin ödeme için satıcı hareketinde depolanmasını sağlayın. Bu, sistemin, alacak hesapları/borç hesapları ana hesabını yeniden oluşturarak sabit boyutlarının dahil edilmesini sağlamaya olanak sağlayacaktır. Sabit boyut değeri ya satıcılarda veya ödeme günlüğü için günlük adında varsayılan değer olarak tanımlanabilir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]