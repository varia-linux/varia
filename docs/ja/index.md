# Variaへようこそ

Varia Linuxは、普段使い向けに設計されたカスタムArch Linuxベースのディストリビューションです。この設定は、Arch Linuxの公式`releng`プロファイルをベースに、作者の個人的な用途に合わせてカスタマイズされています。完全なBudgieデスクトップ環境を提供します。

## 特徴

*   **デスクトップ環境:** Budgie Desktop
*   **ディスプレイマネージャー:** LightDM (slick greeter付き)
*   **ファイルマネージャー:** Nemo
*   **システムツール:** 普段使いを想定していますが、`clonezilla`、`gpart`、`testdisk`、`ddrescue`のようなシステム管理・復旧ツールもいくつか含まれています。
*   **ブート:** レガシーBIOS (Syslinux経由)とモダンなUEFI (systemd-boot経由)の両方のシステムをサポートしています。

## ISOのビルド

Varia LinuxのISOをビルドするには、Arch Linuxシステムに`archiso`パッケージがインストールされている必要があります。

1.  **`archiso`のインストール:**
    ```bash
    sudo pacman -S archiso
    ```

2.  **リポジトリのクローン:**
    ```bash
    git clone <repository-url>
    cd releng
    ```

3.  **ISOのビルド:**
    `releng`ディレクトリ内で`mkarchiso`コマンドを実行します。
    ```bash
    sudo mkarchiso -v -w /tmp/varia-work -o /tmp/varia-out .
    ```
    *   `-v`: 詳細な出力を表示します。
    *   `-w`: 作業ディレクトリを設定します。
    *   `-o`: ISOファイルが作成される出力ディレクトリを設定します。

最終的なISOイメージは、`-o`フラグで指定されたディレクトリ（例: `/tmp/varia-out`）に配置されます。

## 使い方

ISOがビルドされたら、USBドライブに書き込むか、DVDに焼くことができます。作成したメディアからコンピュータを起動すると、Varia Linuxのライブ環境が始まります。