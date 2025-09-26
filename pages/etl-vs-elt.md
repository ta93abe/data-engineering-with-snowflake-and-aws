# ETL vs ELT の違い

<div class="grid grid-cols-2 gap-8 mt-6">

<div v-click="1" class="p-6 bg-gradient-to-br from-blue-50 to-blue-100 rounded-lg">
<h3 class="text-xl font-bold text-blue-800 mb-4">ETL (Extract, Transform, Load)</h3>

<div class="space-y-3">
<div class="flex items-center">
  <div class="w-8 h-8 bg-blue-500 text-white rounded-full flex items-center justify-center text-sm font-bold mr-3">E</div>
  <span>データソースからデータを抽出</span>
</div>
<div class="flex items-center">
  <div class="w-8 h-8 bg-blue-500 text-white rounded-full flex items-center justify-center text-sm font-bold mr-3">T</div>
  <span>外部システムで変換・加工</span>
</div>
<div class="flex items-center">
  <div class="w-8 h-8 bg-blue-500 text-white rounded-full flex items-center justify-center text-sm font-bold mr-3">L</div>
  <span>分析用データベースに読み込み</span>
</div>
</div>

<div class="mt-4 text-sm text-blue-700">
<strong>特徴:</strong> 従来型、データ量が少ない場合に適している
</div>
</div>

<div v-click="2" class="p-6 bg-gradient-to-br from-green-50 to-green-100 rounded-lg">
<h3 class="text-xl font-bold text-green-800 mb-4">ELT (Extract, Load, Transform)</h3>

<div class="space-y-3">
<div class="flex items-center">
  <div class="w-8 h-8 bg-green-500 text-white rounded-full flex items-center justify-center text-sm font-bold mr-3">E</div>
  <span>データソースからデータを抽出</span>
</div>
<div class="flex items-center">
  <div class="w-8 h-8 bg-green-500 text-white rounded-full flex items-center justify-center text-sm font-bold mr-3">L</div>
  <span>生データのまま分析基盤に読み込み</span>
</div>
<div class="flex items-center">
  <div class="w-8 h-8 bg-green-500 text-white rounded-full flex items-center justify-center text-sm font-bold mr-3">T</div>
  <span>分析基盤内で変換・加工</span>
</div>
</div>

<div class="mt-4 text-sm text-green-700">
<strong>特徴:</strong> モダンな手法、大量データ・クラウド環境に適している
</div>
</div>

</div>