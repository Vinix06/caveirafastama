- 👋 Hi, I’m @caveirafastama
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
caveirafastama/caveirafastama is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
private void btnAdicionarActionPerformed(java.awt.event.ActionEvent evt) {                                             
        
        if(rboPC.isSelecet()) {
            tipoComputador = rboPC.getText();
        }else if (rboNotebook.isSelected()) {
            tipoComputador = rboNotebook.getText();
        }else if (rboServidor.isisSelected()) {
            tipoComputador = rboServidor.getText();
        }else {
            JOptionPane.showMessageDialog(this, "Selecione um tipo de PC");
            
                    
        }
    }                                            

    private void btnRomoverActionPerformed(java.awt.event.ActionEvent evt) {                                           
        int indiceLinha = tblCompras.getSelectedRow();
        if (indiceLinha>=0) {
           DefaultTableModel modelo = (DefaultTableModel) tblCompras.getModel();
           modelo.removeRow(indiceLinha);
        }else{
           JOptionPane.showMessageDialog(this, "Selecione uma linha"); 
            
        }
            
        }
        
        
        
    }                                          
       String sistemaOperacional = "";
       if(tgWindows.isSelected()) {
           sistemaOperacional = tgWindows.getText();
           
           String tipoHD = "";
           tipoHD = cboHD.getSelected().toString();
           
           
           String acessorios = "";
           if(chkMochila.isSelected()) {
              acessorios += chkMochila.getText() + ", ";
              
           }
               if(chkHUB.isSelected()) {
              acessorios += chkHUB.getText() + ", ";
              
              if(chkMouse.isSelected()) {
              acessorios += chkMouse.getText() + ", ";
           }
           
           
       }
    
    String itensLista = "";
    List<String>listaItens = lstServicos.getSelectedValuesList;
    
    for (String item : listaItens) {
        itensLista += item + ", ";
        
    }
        
    DefaultTableModel modelo = (DefaultTableModel) tblCompras.getModel();
    modelo.addRow(new String[] {tipoComputador,
                                sistemaOperacional,
                                tipoHD,
                                acessorios
                                itensLista        
                                    
    },

    
    /**
     * @param args the command line arguments
     */
    public static void main(String args[]) {
        /* Set the Nimbus look and feel */
        //<editor-fold defaultstate="collapsed" desc=" Look and feel setting code (optional) ">
        /* If Nimbus (introduced in Java SE 6) is not available, stay with the default look and feel.
         * For details see http://download.oracle.com/javase/tutorial/uiswing/lookandfeel/plaf.html 
         */
        try {
            for (javax.swing.UIManager.LookAndFeelInfo info : javax.swing.UIManager.getInstalledLookAndFeels()) {
                if ("Nimbus".equals(info.getName())) {
                    javax.swing.UIManager.setLookAndFeel(info.getClassName());
                    break;
                }
            }
        } catch (ClassNotFoundException ex) {
            java.util.logging.Logger.getLogger(TelaVendaComputador.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (InstantiationException ex) {
            java.util.logging.Logger.getLogger(TelaVendaComputador.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (IllegalAccessException ex) {
            java.util.logging.Logger.getLogger(TelaVendaComputador.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (javax.swing.UnsupportedLookAndFeelException ex) {
            java.util.logging.Logger.getLogger(TelaVendaComputador.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        }
        //</editor-fold>

        /* Create and display the form */
        java.awt.EventQueue.invokeLater(new Runnable() {
            public void run() {
                new TelaVendaComputador().setVisible(true);
            }
        });
    }

    // Variables declaration - do not modify                     
    private javax.swing.ButtonGroup bgSO;
    private javax.swing.ButtonGroup bgtipoComputador;
    private javax.swing.JButton btnAdicionar;
    private javax.swing.JButton btnRomover;
    private javax.swing.JLabel cboHD;
    private javax.swing.JCheckBox chkHUBUSB;
    private javax.swing.JCheckBox chkMochila;
    private javax.swing.JCheckBox chkMouseGamer;
    private javax.swing.JButton jButton1;
    private javax.swing.JButton jButton2;
    private javax.swing.JComboBox<String> jComboBox1;
    private javax.swing.JList<String> jList1;
    private javax.swing.JPanel jPanel1;
    private javax.swing.JPanel jPanel2;
    private javax.swing.JPanel jPanel3;
    private javax.swing.JPanel jPanel4;
    private javax.swing.JPanel jPanel5;
    private javax.swing.JScrollPane jScrollPane1;
    private javax.swing.JScrollPane jScrollPane2;
    private javax.swing.JPanel lstServicos;
    private javax.swing.JRadioButton rboNotebook;
    private javax.swing.JRadioButton rboServidor;
    private javax.swing.JRadioButton rdoPC;
    private javax.swing.JTable tblCompras;
    private javax.swing.JToggleButton tgLinux;
    private javax.swing.JToggleButton tgWindows;
    // End of variables declaration                   
}
