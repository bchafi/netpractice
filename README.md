<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Networking Fundamentals</title>
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-50 text-gray-800">
  <!-- Header -->
  <header class="bg-gradient-to-r from-blue-600 to-indigo-700 text-white py-6 shadow-md">
    <div class="max-w-5xl mx-auto px-6 flex justify-between items-center">
      <h1 class="text-2xl font-bold">🌐 Networking Fundamentals</h1>
      <nav class="space-x-6">
        <a href="#ip" class="hover:underline">IP</a>
        <a href="#tcp" class="hover:underline">TCP</a>
        <a href="#tcpip" class="hover:underline">TCP/IP</a>
        <a href="#osi" class="hover:underline">OSI Model</a>
      </nav>
    </div>
  </header>

  <!-- Hero Section -->
  <section class="text-center py-16 bg-white shadow-sm">
    <h2 class="text-4xl font-extrabold text-blue-700">Master the Basics of Networking</h2>
    <p class="mt-4 text-lg text-gray-600">IP, TCP, TCP/IP, OSI Model explained in simple terms with examples 🚀</p>
  </section>

  <!-- IP Section -->
  <section id="ip" class="max-w-5xl mx-auto px-6 py-12">
    <h3 class="text-2xl font-bold text-indigo-700 mb-4">1. IP (Internet Protocol)</h3>
    <p class="mb-4">IP defines how devices identify and locate each other on a network and how data packets are delivered.</p>
    <ul class="list-disc pl-6 space-y-2">
      <li><b>Main role:</b> Addressing and routing</li>
      <li><b>Analogy:</b> Like your home address for the internet</li>
      <li><b>Versions:</b> IPv4 (32-bit, ~4.3B addresses) and IPv6 (128-bit, ~340 undecillion addresses)</li>
    </ul>
    <div class="bg-gray-100 rounded-xl p-4 mt-4">
      <p><b>IPv4 Example:</b> 192.168.1.10</p>
      <p><b>IPv6 Example:</b> 2001:0db8::1</p>
    </div>
  </section>

  <!-- TCP Section -->
  <section id="tcp" class="max-w-5xl mx-auto px-6 py-12 bg-gray-50">
    <h3 class="text-2xl font-bold text-indigo-700 mb-4">2. TCP (Transmission Control Protocol)</h3>
    <p class="mb-4">TCP ensures reliable communication between devices.</p>
    <ul class="list-disc pl-6 space-y-2">
      <li>Breaks data into packets</li>
      <li>Numbers and checks packets for errors</li>
      <li>Resends lost packets</li>
      <li>Reassembles packets in correct order</li>
    </ul>
    <p class="mt-4"><b>Analogy:</b> Like a phone call where each message is acknowledged.</p>
  </section>

  <!-- TCP/IP Section -->
  <section id="tcpip" class="max-w-5xl mx-auto px-6 py-12">
    <h3 class="text-2xl font-bold text-indigo-700 mb-4">3. TCP/IP</h3>
    <p class="mb-4">TCP/IP is the foundation of the Internet.</p>
    <ul class="list-disc pl-6 space-y-2">
      <li><b>IP:</b> Handles addressing and routing (where data goes)</li>
      <li><b>TCP:</b> Ensures reliable delivery (how data arrives)</li>
    </ul>
    <div class="bg-gray-100 rounded-xl p-4 mt-4">
      <p>📦 Data → split by TCP → wrapped with IP address → sent → received → rebuilt by TCP</p>
    </div>
  </section>

  <!-- OSI Model Section -->
  <section id="osi" class="max-w-5xl mx-auto px-6 py-12 bg-gray-50">
    <h3 class="text-2xl font-bold text-indigo-700 mb-4">4. OSI Model</h3>
    <p class="mb-4">The OSI model standardizes how different systems communicate, using 7 layers.</p>
    <ol class="list-decimal pl-6 space-y-1">
      <li>Application – User interaction</li>
      <li>Presentation – Data encryption & formatting</li>
      <li>Session – Manage communication sessions</li>
      <li>Transport – Reliable delivery (TCP/UDP)</li>
      <li>Network – Addressing & routing (IP)</li>
      <li>Data Link – Local delivery (MAC)</li>
      <li>Physical – Wires, signals, connectors</li>
    </ol>
    <div class="bg-gray-100 rounded-xl p-4 mt-4">
      <p><b>Analogy:</b> Like a blueprint for how data travels from one computer to another.</p>
    </div>
  </section>

  <!-- Footer -->
  <footer class="bg-indigo-700 text-white text-center py-6 mt-12">
    <p>⚡ Built for learning Networking · Hosted on GitHub Pages</p>
  </footer>
</body>
</html>
