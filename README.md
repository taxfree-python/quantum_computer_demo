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
