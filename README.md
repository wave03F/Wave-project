สมาทโฟน

import 'package:flutter/material.dart';
import 'package:google_fonts/google_fonts.dart';

import 'Character.dart';
import 'Conten.dart';

//oid main() => runApp(DemoFontPage());
//void main() => runApp(CardWidget2());

//void main() => runApp(MyApp());

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: HomeScreen(),
    );
  }
}

class HomeScreen extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('WM'),
        centerTitle: true,
      ),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: [
            Text(
              'Project MW',
              style: TextStyle(
                fontSize: 32,
                fontWeight: FontWeight.bold,
              ),
            ),
            SizedBox(height: 50),
            ElevatedButton(
              onPressed: () {
                Navigator.push(context,
                    MaterialPageRoute(builder: (ctx) => ContentPage()));
                // กำหนดฟังก์ชันเมื่อกดปุ่มนี้
                // กำหนดฟังก์ชันเมื่อกดปุ่มนี้
              },
              child: Padding(
                padding:
                    const EdgeInsets.symmetric(horizontal: 20, vertical: 15),
                child: Text(
                  'เนื้อเรื่อง',
                  style:
                      GoogleFonts.itim(fontSize: 20, color: Color(0xff000000)),
                ),
              ),
            ),
            SizedBox(height: 20),
            ElevatedButton(
              onPressed: () {
                Navigator.push(context,
                    MaterialPageRoute(builder: (ctx) => CharacterListPage()));
                // กำหนดฟังก์ชันเมื่อกดปุ่มนี้
              },
              child: Padding(
                padding:
                    const EdgeInsets.symmetric(horizontal: 20, vertical: 15),
                child: Text(
                  'ตัวละคร',
                  style:
                      GoogleFonts.itim(fontSize: 20, color: Color(0xff000000)),
                ),
              ),
            ),
          ],
        ),
      ),
    );
  }
}
