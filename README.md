import 'package:flutter/material.dart';

void main() {
  runApp(const MaterialApp(
    home: PostScreen(),
    debugShowCheckedModeBanner: false,
  ));
}

class PostScreen extends StatelessWidget {
  const PostScreen({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      backgroundColor: Colors.blue[50],
      body: SafeArea(
        child: Column(
          children: [
            const SizedBox(height: 10),
            ListTile(
              leading: CircleAvatar(
                backgroundImage: NetworkImage('https://i.pravatar.cc/150?img=58'),
              ),
              title: const Text("Sophie Turner", style: TextStyle(fontWeight: FontWeight.bold)),
              subtitle: const Text("@sophieT"),
              trailing: const Icon(Icons.more_vert),
            ),
            const Padding(
              padding: EdgeInsets.symmetric(horizontal: 16.0, vertical: 8.0),
              child: Text(
                "Just explored a serene forest trail this morning.🌅 The calm of the trees and chirping of the birds were magical. Days like this make me appreciate the beauty around us🤌🏻",
              ),
            ),
            Container(
              margin: const EdgeInsets.symmetric(horizontal: 16),
              height: 200,
              decoration: BoxDecoration(
                borderRadius: BorderRadius.circular(16),
                image: const DecorationImage(
                  image: NetworkImage('https://images.unsplash.com/photo-1506748686214-e9df14d4d9d0'),
                  fit: BoxFit.cover,
                ),
              ),
            ),
            const SizedBox(height: 12),
            Padding(
              padding: const EdgeInsets.symmetric(horizontal: 16.0),
              child: Row(
                children: const [
                  Icon(Icons.favorite_border),
                  SizedBox(width: 30),
                  Icon(Icons.chat_bubble_outline),
                  SizedBox(width: 30),
                  Icon(Icons.share),
                ],
              ),
            ),
            const Padding(
              padding: EdgeInsets.symmetric(horizontal: 16.0, vertical: 8),
              child: Text("15k likes", style: TextStyle(fontWeight: FontWeight.w500)),
            ),
            const Padding(
              padding: EdgeInsets.symmetric(horizontal: 10.0),
              child: Column(
                crossAxisAlignment: CrossAxisAlignment.start,
                children: [
                  Text("💫In silence, peace speaks the loudest"),
                  Text("🌍Peace is the language that every heart understands"),
                ],
              ),
            ),
            const Spacer(),
            const Divider(height: 1),
            ListTile(
              leading: CircleAvatar(
                backgroundImage: NetworkImage('https://i.pravatar.cc/150?img=32'),
              ),
              title: const TextField(
                decoration: InputDecoration.collapsed(
                  hintText: "Add a comment...",
                ),
              ),
            ),
          ],
        ),
      ),
    );
  }
}
