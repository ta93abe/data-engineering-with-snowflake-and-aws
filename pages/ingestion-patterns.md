# データ取り込みの3つのパターン

<div class="grid grid-cols-1 gap-6 mt-6">

<div v-click="1" class="flex items-center p-4 border-l-4 border-blue-500 bg-blue-50">
<div class="flex-shrink-0 w-12 h-12 bg-blue-500 text-white rounded-full flex items-center justify-center font-bold mr-4">1</div>
<div>
  <h3 class="font-semibold text-blue-800">バッチ処理（Batch Processing）</h3>
  <p class="text-blue-600 text-sm mt-1">定期的にまとまったデータを処理。日次、時間単位など</p>
</div>
</div>

<div v-click="2" class="flex items-center p-4 border-l-4 border-green-500 bg-green-50">
<div class="flex-shrink-0 w-12 h-12 bg-green-500 text-white rounded-full flex items-center justify-center font-bold mr-4">2</div>
<div>
  <h3 class="font-semibold text-green-800">リアルタイム処理（Real-time Processing）</h3>
  <p class="text-green-600 text-sm mt-1">データが生成されるとすぐに処理。ミリ秒～秒単位</p>
</div>
</div>

<div v-click="3" class="flex items-center p-4 border-l-4 border-yellow-500 bg-yellow-50">
<div class="flex-shrink-0 w-12 h-12 bg-yellow-500 text-white rounded-full flex items-center justify-center font-bold mr-4">3</div>
<div>
  <h3 class="font-semibold text-yellow-800">ニアリアルタイム処理（Near Real-time）</h3>
  <p class="text-yellow-600 text-sm mt-1">準リアルタイム。数分～数時間の遅延</p>
</div>
</div>

</div>