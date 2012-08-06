package com.sdc.android.UDExam.Fragments;

import com.sdc.android.UDExam.Swipeytabs.R;
import com.sdc.android.UDExam.Swipeytabs.R.id;

import android.os.Bundle;
import android.support.v4.app.Fragment;
import android.view.ContextMenu;
import android.view.LayoutInflater;
import android.view.MenuItem;
import android.view.View;
import android.view.View.OnClickListener;
import android.view.ViewGroup;
import android.widget.Button;
import android.widget.LinearLayout;
import android.widget.TextView;

public class AdvancedTestFragment extends Fragment implements OnClickListener{
	private Button bt_choise_subject_av;
	private TextView subject_av, suggest_av, note_advanced_test;
	private String[] SUBJECTS;
	private LinearLayout linear_subject, linear_suggest;
	@Override
    public View onCreateView(LayoutInflater inflater, ViewGroup container, Bundle savedInstanceState) {
        ViewGroup root = (ViewGroup) inflater.inflate(R.layout.advanced_test, null);
        SUBJECTS = getResources().getStringArray(R.array.subjects);
        bt_choise_subject_av = (Button) root.findViewById(id.bt_choise_subject_av);
        bt_choise_subject_av.setOnClickListener(this);
        subject_av = (TextView) root.findViewById(id.subject_av);
        suggest_av = (TextView) root.findViewById(id.suggest_av);
        linear_subject = (LinearLayout) root.findViewById(id.onChoiseSubject_av);
        linear_subject.setOnClickListener(this);
        linear_suggest = (LinearLayout) root.findViewById(id.onChoiseSuggest_av);
        linear_suggest.setOnClickListener(this);
        note_advanced_test = (TextView) root.findViewById(id.note_advanced_test);
        note_advanced_test.setOnClickListener(this);
        note_advanced_test.setSelected(true);
        this.registerForContextMenu(bt_choise_subject_av);
        return root;
	}
	@Override
	public void onClick(View v) {
		if(v.getId() == id.bt_choise_subject_av || v.getId() == id.onChoiseSubject_av){
			bt_choise_subject_av.showContextMenu();
		}
		
		if(v.getId() == id.onChoiseSuggest_av){
			if(suggest_av.getText().toString().trim().equals(getResources().getString(R.string.yes))) 
				suggest_av.setText(R.string.no);
			else
				suggest_av.setText(R.string.yes);
		}
		
		if(v.getId() == id.note_advanced_test){
			note_advanced_test.setSelected(false);
			note_advanced_test.setSelected(true);
		}
	}
	
	@Override
	public void onCreateContextMenu(ContextMenu menu, View v, ContextMenu.ContextMenuInfo menuInfo) {
		createMenu(menu);
	}

	private void createMenu(ContextMenu menu) {
		for(String sub : SUBJECTS){
			menu.add(sub);
		}
	}
	
	@Override
	public boolean onContextItemSelected(MenuItem item) {
		return(applyMenuChoice(item) ||
  		super.onContextItemSelected(item));
  }

	private boolean applyMenuChoice(MenuItem item) {
		subject_av.setText(item.getTitle());
		return true;
	}
}
