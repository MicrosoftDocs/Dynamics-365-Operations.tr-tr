---
title: ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 3 - Biçimi oluşturma)
description: Bu makalede, ER çıktılarında Belge Yönetimi dosyaları kullanmak üzere Elektronik raporlama biçiminin nasıl yapılandırılacağı açıklanmaktadır. (3. Bölüm)
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
ms.openlocfilehash: b70f5ed74fd701be79daebbd2a8f246a0a0ab95e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290949"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a>ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 3 - Biçimi oluşturma)

[!include [banner](../../includes/banner.md)]

Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının, ER çıktısında Belge Yönetimi belgelerini (eklerini) kullanmak amacıyla bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar. Bu adımlar tüm şirketlerde gerçekleştirilebilir.

Bu adımları tamamlamak için öncelikle "ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 2: Veri modelini genişletme" yordamındaki adımları tamamlamalısınız.

Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.


## <a name="create-a-format-to-process-invoices"></a>Faturaları işlemek için bir biçim oluşturma
1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
2. Raporlama konfigürasyonları'na tıklayın.
3. Ağaçta "Müşteri fatura modeli" seçeneğini genişletin.
4. Ağaçta, "Müşteri faturası modeli\Müşteri faturası modeli (özel)" seçeneğini seçin.
    * Faturayı elektronik işlemeyle ilgili bir satış siparişine eklenmiş her türlü dosya hakkındaki bilgilerle elektronik iletiler oluşturmak için bir biçim oluşturursunuz.  
5. İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.
6. Yeni alanına, "Müşteri faturası modeli (özel) veri modeline bağlı biçim" yazın.
7. Ad alanına "Elektronik fatura örnek iletisi" yazın.
    * Elektronik fatura örnek iletisi  
8. Veri modeli tanımı alanına bir değer girin veya seçin.
    * InvoiceCustomer  
9. Konfigürasyon oluştur'u tıklatın.

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a>Ekleri oluşturulan iletiye MIME biçiminde doldurmak için bir biçim tasarlama
1. Tasarımcı'yı tıklatın.
2. İletişim kutusunu açmak için Kök ekle'yi tıklatın.
3. Ağaçta seçin 'XML\Element'.
4. Ad alanına "Fatura" yazın.
    * Fatura  
5. Tamam'a tıklayın.
6. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
7. Ağaçta seçin 'XML\Attribute'.
8. Ad alanına "SalesOrder" yazın.
    * SalesOrder  
9. Tamam'a tıklayın.
10. Öznitelik Ekle'ye tıklayın.
11. Ad alanına "InvoiceNumber" yazın.
    * InvoiceNumber  
12. Tamam'a tıklayın.
13. Öznitelik Ekle'ye tıklayın.
14. Ad alanına "InvoiceAmount" yazın.
    * InvoiceAmount  
15. Tamam'a tıklayın.
16. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
17. Ağaçta seçin 'XML\Element'.
18. Ad alanına "EnclosedDocs" yazın.
    * EnclosedDocs  
19. Tamam'a tıklayın.
20. Ağaçta, "Fatura\EnclosedDocs" seçeneğini işaretleyin.
21. Öğe Ekle'ye tıklayın.
22. Ad alanına "Belge" yazın.
    * Belge  
23. Tamam'a tıklayın.
24. Ağaçta, "Fatura\EnclosedDocs\Belge" seçeneğini işaretleyin.
25. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
26. Ağaçta seçin 'XML\Attribute'.
27. Ad alanına "FileName" yazın.
    * FileName  
28. Tamam'a tıklayın.
29. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
30. Ağaçta seçin 'XML\Element'.
31. Ad alanına "FileContent" yazın.
    * FileContent  
32. Tamam'a tıklayın.
33. Ağaçta, "Fatura\EnclosedDocs\Belgeler\FileContent" seçeneğini işaretleyin.
34. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
35. Ağaçta, "Metin\Base64" seçeneğini işaretleyin.
36. Tamam'a tıklayın.

## <a name="map-format-elements-to-data-model-as-data-source"></a>Veri kaynağı olarak veri modeline biçim öğelerini eşleme
1. Ağaçta, "Fatura\SalesOrder" seçeneğini işaretleyin.
2. Eşleme sekmesini tıklatın.
3. Ağaçta, 'model'i genişletin.
4. Ağaçta, "model\Satış siparişi numarası(SalesId)" seçeneğini işaretleyin.
5. Bağla'ya tıklayın.
6. Ağaçta, "Fatura\InvoiceNumber" seçeneğini işaretleyin.
7. Ağaçta, "model\Temel fatura(InvoiceBase)" seçeneğini genişletin.
8. Ağaçta, "model\Temel fatura(InvoiceBase)\Fatura numarası(Id)" seçeneğini işaretleyin.
9. Bağla'ya tıklayın.
10. Ağaçta, "Fatura\InvoiceAmount" seçeneğini işaretleyin.
11. Ağaçta, "model\Temel fatura(InvoiceBase)\Fatura tutarı(Tutar)" seçeneğini işaretleyin.
12. Bağla'ya tıklayın.
13. Ağaçta, "model\Fatura ekleri" seçeneğini genişletin.
14. Ağaçta, "model\Fatura ekleri\Dosya içeriği" seçeneğini işaretleyin.
15. Ağaçta, "Fatura\EnclosedDocs\Belge\FileContent\Base64" seçeneğini işaretleyin.
16. Bağla'ya tıklayın.
17. Ağaçta "model\Fatura ekleri\Dosya adı" seçeneğini işaretleyin.
18. Ağaçta, "Fatura\EnclosedDocs\Belgeler\FileName" seçeneğini işaretleyin.
19. Bağla'ya tıklayın.
20. Ağaçta, "model\Fatura ekleri" seçeneğini işaretleyin.
21. Ağaçta, "Fatura\EnclosedDocs\Belge" seçeneğini işaretleyin.
22. Bağla'ya tıklayın.
23. Kaydet'e tıklayın.
24. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
