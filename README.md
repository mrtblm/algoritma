Test Otomasyon Eğitimi 6.Ödev

package org.testodev;

import javax.swing.*;
import java.util.HashMap;
import java.util.Map;

public class Main {
    public static void main(String[] args) {

        String[] metinDizisi = {"Merhaba", "Murat", "Bilim", "Test", "Otomasyon", "Kursu"};

        String yeniMetin = algoritma(metinDizisi);
        System.out.println("Oluşturulan Yeni Metin : " + yeniMetin);
        JOptionPane.showMessageDialog(null,"Oluşturulan Yeni Metin: \n" + yeniMetin);

    }

    public static String algoritma(String[] metinDizisi) {
        StringBuilder birlesmisMetin = new StringBuilder();

        for (String metin : metinDizisi) {
            for (int i = 0; i < metin.length(); i++) {
                char karakter = metin.charAt(i);

                // Yeni metinde bu karakter daha önce yoksa ekle
                if (birlesmisMetin.indexOf(String.valueOf(karakter)) == -1) {
                    birlesmisMetin.append(karakter);
                }
            }
        }

        return birlesmisMetin.toString();


    }
}
