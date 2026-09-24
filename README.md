<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>منصة العراق التعليمية - لوحة التحكم</title>
    <style>
        * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; }
        body { background-color: #f4f6f9; color: #333; display: flex; flex-direction: column; min-height: 100vh; }
        
        /* الهيدر */
        header { background-color: #1a252f; color: white; padding: 15px 20px; display: flex; justify-content: space-between; align-items: center; }
        header h1 { font-size: 20px; }
        .user-info { font-size: 14px; background: #2c3e50; padding: 5px 12px; border-radius: 15px; }

        /* الحاوية الرئيسية */
        .main-container { display: flex; flex: 1; }

        /* القائمة الجانبية */
        .sidebar { width: 220px; background-color: #2c3e50; color: white; padding: 20px 0; }
        .sidebar ul { list-style: none; }
        .sidebar li a { display: block; padding: 12px 20px; color: #ecf0f1; text-decoration: none; font-size: 15px; transition: 0.3s; }
        .sidebar li a:hover, .sidebar li a.active { background-color: #34495e; border-right: 4px solid #3498db; }

        /* محتوى لوحة التحكم */
        .content { flex: 1; padding: 25px; }
        .dashboard-header { margin-bottom: 25px; }
        
        /* بطاقات الإحصائيات */
        .stats-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 20px; margin-bottom: 30px; }
        .card { background: white; padding: 20px; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.05); text-align: center; }
        .card h3 { color: #7f8c8d; font-size: 14px; margin-bottom: 10px; }
        .card p { font-size: 28px; font-weight: bold; color: #2c3e50; }

        /* الجدول */
        .table-section { background: white; padding: 20px; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.05); }
        .table-section h3 { margin-bottom: 15px; color: #2c3e50; }
        table { width: 100%; border-collapse: collapse; text-align: right; }
        th, td { padding: 12px 15px; border-bottom: 1px solid #ddd; }
        th { background-color: #f8f9fa; color: #333; }
        .status { padding: 4px 8px; border-radius: 4px; font-size: 12px; font-weight: bold; }
        .status.active { background-color: #e8f8f5; color: #27ae60; }
        .status.pending { background-color: #fef9e7; color: #f39c12; }

        @media (max-width: 768px) {
            .main-container { flex-direction: column; }
            .sidebar { width: 100%; }
        }
    </style>
</head>
<body>

    <header>
        <h1>منصة العراق التعليمية 🇮🇶</h1>
        <div class="user-info">المدير: محمد</div>
    </header>

    <div class="main-container">
        <!-- القائمة الجانبية -->
        <div class="sidebar">
            <ul>
                <li><a href="#" class="active">الرئيسية</a></li>
                <li><a href="#">الطلاب</a></li>
                <li><a href="#">المناهج والدروس</a></li>
                <li><a href="#">التقارير</a></li>
                <li><a href="#">الإعدادات</a></li>
            </ul>
        </div>

        <!-- المحتوى الرئيسي -->
        <div class="content">
            <div class="dashboard-header">
                <h2>لوحة التحكم الإدارية</h2>
                <p>مرحباً بك! هذه نظرة عامة على نشاط المنصة اليوم.</p>
            </div>

            <!-- بطاقات الإحصائيات -->
            <div class="stats-grid">
                <div class="card">
                    <h3>إجمالي الطلاب</h3>
                    <p id="student-count">1,250</p>
                </div>
                <div class="card">
                    <h3>الدورات المتاحة</h3>
                    <p>48</p>
                </div>
                <div class="card">
                    <h3>الامتحانات النشطة</h3>
                    <p>12</p>
                </div>
                <div class="card">
                    <h3>نسبة الإنجاز</h3>
                    <p>89%</p>
                </div>
            </div>

            <!-- جدول أحدث الطلاب -->
            <div class="table-section">
                <h3>أحدث الطلاب المسجلين</h3>
                <table>
                    <thead>
                        <tr>
                            <th>اسم الطالب</th>
                            <th>المرحلة الدراسية</th>
                            <th>تاريخ التسجيل</th>
                            <th>الحالة</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>أحمد علي</td>
                            <td>السادس الإعدادي</td>
                            <td>2026-09-24</td>
                            <td><span class="status active">نشط</span></td>
                        </tr>
                        <tr>
                            <td>مريم حسين</td>
                            <td>الثالث المتوسط</td>
                            <td>2026-09-23</td>
                            <td><span class="status active">نشط</span></td>
                        </tr>
                        <tr>
                            <td>عمر خالد</td>
                            <td>الرابع العلمي</td>
                            <td>2026-09-22</td>
                            <td><span class="status pending">قيد الانتظار</span></td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>
    </div>

</body>
</html>
