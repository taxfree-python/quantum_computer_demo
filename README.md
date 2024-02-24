# quantum_computer_demo
量子コンピュータ本輪読のデモを載せていきたい

## qc_demo_bloch_vector
任意のノルムが 1 のベクトルを Bloch sphere 上で可視化できる．

初期状態は
```
theta = np.pi / 4
phi = np.pi / 2
```
で定義されているので，これらの角度を調整することで好きなベクトルを表現できる．

また，
```
qc = QuantumCircuit(1)
qc.x(0)
```
の部分に好きな [qiskit](https://qiita.com/tare_/items/0753a977de9d8d3348a2) 上の回路を実装することで，その回路の前後での変化を確認できる．

## qc_demo_fig_2_2
P.23 の量子回路を Qiskit 上で実装し Aer を用いてシミュレートしている．
```
circ = qiskit.QuantumCircuit(3)

circ.h(0)
circ.h(2)

circ.cx(0, 1)
circ.cz(1, 2)

circ.h(2)
```
今回は図 2.2 を実装したが，上の部分を編集することで好きな回路を実装できる．
また，IBM Q のアカウントを取得して少しソースコードを編集するとクラウド経由で実機でも動かせる(たぶん，これから実装する)
